<template>
  <div class="project-details">
    <div class="project-left">
      <div class="project-header">
        <h1>Int to Roman</h1>
      </div>
      <div class="project-body">
        <form>
          <div class="formtext"><input id="inpuut" v-model.lazy="user_input" type="text" ></div>
          <div class="formsubmit"><button @click="domSubmit()">Crunch</button></div>
          <div class="formclear"><button @click="domClear()">Clear</button></div>
        </form>
        <section class="results">Output: <span id="calcoutput">{{intToRoman(this.enteredInt)}}</span></br></section>
        <section class="controls"><span id="error-message">{{errorMessage}}</span></section>
      </div>
    </div>

    <div class="project-right">
      <div class="project-header">
        <h1>About</h1>
      </div>
      <div class="project-body">
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quo provident libero deserunt placeat iste quisquam. Rem a eum perspiciatis, natus sunt tempora facere laboriosam fugit porro quas deserunt maiores. Recusandae.</p>
      </div>
      <div class="project-footer">
        <img src="../assets/html_logo.png" alt="HTML Utilized">
        <img src="../assets/css_logo.png" alt="CSS Utilized">
        <img src="../assets/js_logo.png" alt="Javascript Utilized">
        <br>
        <img src="../assets/github_logo.png" alt="Github">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IntToRoman",
  data() {
    return {
      num: "1991",
      enteredInt: "1991",
      errorMessage: "",
      user_input: "1991",
      romNum: "",
      parsed: ""
    };
  },
  computed: {
  },
  methods: {
    domClear() {
      this.user_input = "1"
      this.enteredInt = "1"
      console.log('Resetting the form')
    },
    domSubmit() {
      this.enteredInt = this.user_input;
      console.log(this.enteredInt + " submitted");
      this.intToRoman(this.enteredInt);
    },
    errorFade() {
      this.errorMessage = ""
    },
    intToRoman(num) {
      if (this.enteredInt > 0 && this.enteredInt < 4000) {
        //Convert Int => String
        var input = "" + num;
        //reverse number
        var revNum = "";
        var romNum = "";
        for (let i = input.length - 1; i >= 0; i--) {
          revNum += input[i];
        }
        //break up number into places
        var places = {
          ones: revNum[0],
          tens: revNum[1],
          hundreds: revNum[2],
          thousands: revNum[3]
        };
        console.log(places);

        //Hash this out!!!
        //Thousands
        if (places.thousands > 0 && places.thousands <= 3) {
          for (let i = 1; i <= places.thousands; i++) {
            romNum += "M";
          }
        }
        //Hundreds
        if (places.hundreds > 0 && places.hundreds <= 3) {
          for (let i = 1; i <= places.hundreds; i++) {
            romNum += "C";
          }
        } else if (places.hundreds == 4) {
          romNum += "CD";
        } else if (places.hundreds == 5) {
          romNum += "D";
        } else if (places.hundreds >= 6 && places.hundreds <= 8) {
          romNum += "D";
          for (let i = 5; i <= places.hundreds - 1; i++) {
            romNum += "C";
          }
        } else if (places.hundreds == 9) {
          romNum += "CM";
        }
        //Tens
        if (places.tens > 0 && places.tens <= 3) {
          for (let i = 1; i <= places.tens; i++) {
            romNum += "X";
          }
        } else if (places.tens == 4) {
          romNum += "XL";
        } else if (places.tens == 5) {
          romNum += "L";
        } else if (places.tens >= 6 && places.tens <= 8) {
          romNum += "L";
          for (i = 5; i <= places.tens - 1; i++) {
            romNum += "X";
          }
        } else if (places.tens == 9) {
          romNum += "XC";
        }

        //Ones
        if (places.ones > 0 && places.ones <= 3) {
          for (let i = 1; i <= places.ones; i++) {
            romNum += "I";
          }
        } else if (places.ones == 4) {
          romNum += "IV";
        } else if (places.ones == 5) {
          romNum += "V";
        } else if (places.ones >= 6 && places.ones <= 8) {
          romNum += "V";
          for (let i = 5; i <= places.ones - 1; i++) {
            romNum += "I";
          }
        } else if (places.ones == 9) {
          romNum += "IX";
        }

        console.log(romNum);
        this.romNum = romNum;
        return romNum;
        //document.getElementById("calcoutput").innerText = intToRoman(val);
        //document.getElementById("calcinput").innerText = val;
      } else {
        this.errorMessage = "Must be a number between 1-3999";
        console.log("Invalid")
        this.user_input = "1"
        this.enteredInt = "1"
        self.setTimeout(this.errorFade, 3000);
        return
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#error-message{
  color: red;
}

.project-details {
  font-size: 1.5rem;
  color: var(--light);
  display: grid;
  grid-gap: 10px;
  grid-template-columns: 1fr 2fr;
  text-align: center;
  text-justify: auto;
}

.project-left {
  border-radius: var(--rounded);
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
  grid-template-areas:
    "project-header"
    "project-body";
  height: var(--card-height);
  box-shadow: var(--shadow);
  align-items: center;
  text-align: center;
  text-justify: auto;
  background-color: lightblue;
}

.project-right {
  border-radius: var(--rounded);
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
  grid-template-areas:
    "project-header"
    "project-body"
    "project-footer";
  height: var(--card-height);
  box-shadow: var(--shadow);
  align-items: center;
  text-align: center;
  text-justify: auto;
  background-color: orange;
}

.project-details img {
  height: 4rem;
  opacity: 1;
  margin: 0px;
  padding: 0px;
}
</style>
