<template>
  <div>
    <div class="row">
      <div class="col-sm-3 text-center side">
        <img src="http://image.ibb.co/nQwcqk/Raj_Desai_5.png" alt="Raj_Desai_5" border="0">
        <img src="http://image.ibb.co/gDKK35/4.png" alt="4" border="0">
      </div>

      <div class="col-sm-3 col-sm-offset-9 side">
        <br>
        <img src="http://image.ibb.co/muxHqk/Raj_Desai_4.png" alt="Raj_Desai_4" border="0">
        <h3>Let's Chat!</h3>
        <form>
          <input v-model="name" placeholder="Name" required><br><br>
          <input v-model="email" type="email" placeholder="Email" required><br><br>
          <input v-model="subject" placeholder="Subject" required><br><br>
          <textarea v-model="message" rows="6" placeholder="Message" required></textarea>
          <hr class="offwhite">
          <div class="row">
            <div class="col-sm-6 text-left">
              <div @click="contactMe()" class="well well-sm text-center" title="Submit Your Message!">
                <span class="glyphicon glyphicon-send"></span>
              </div>
            </div>
            <div @click="resetFields()" class="col-sm-6 text-right">
              <div class="well well-sm text-center" title="Reset Your Message!">
                <span class="glyphicon glyphicon-trash"></span>
              </div>
            </div>
          </div>
        </form>
      </div>
    </div>

    <div class="row">
      <nav class="navbar navbar-default navbar-fixed-top">
        <div class="col-sm-6 col-sm-offset-3 text-center logo">
          <div class="col-sm-3">
            <a href="#fun"><li class="list-group-item">Bored?</li></a>
          </div>
          <div class="col-sm-3">
            <a href="#accordion"><li class="list-group-item">My Projects</li></a>
          </div>
          <div class="col-sm-3">
            <a target="_blank" href="https://www.github.com/RADesai"><li class="list-group-item"><i class="fa fa-github" aria-hidden="true"></i></li></a>
          </div>
          <div class="col-sm-3">
            <a target="_blank" href="https://www.linkedin.com/in/rajadesai"><li class="list-group-item"><i class="fa fa-linkedin" aria-hidden="true"></i></li></a>
          </div>
        </div>
      </nav>
    </div>

    <div class="apps" data-spy="scroll">
      <div class="row">
        <div class="col-sm-2 col-sm-offset-3">
          <h2>Hi There!</h2>
          <h3>I'm Raj</h3>
        </div>
        <div class="col-sm-4">
          <img src="http://image.ibb.co/nsFR0k/basketball_bg.png" alt="basketball_bg" border="0">
        </div>
      </div>
      <div class="row">
        <div class="col-sm-6 col-sm-offset-3">
          <br><br>
        </div>
      </div>
      <div class="row" id="fun">
        <div class="col-sm-6 col-sm-offset-3">
          <h3>Bored? Check these out:</h3>
          <hr>
        </div>
        <div class="col-sm-3 col-sm-offset-3">
          <h4>I firmly believe that it isn't right to objectify anyone, unless it's in JSON!</h4>
          <h5>Find the character that would remove the syntax error to reveal a hidden image!</h5>
          <img src="http://image.ibb.co/m4eDVk/Raj_Desai_3.png" alt="Raj_Desai_3" border="0">
          <input v-model="guess" placeholder="**HINT: It rhymes with 'llama'**"><br><br>
        </div>
        <div v-if="guessedRight()" class="col-sm-3">
          <img class="img-rounded" src="http://image.ibb.co/kc4m0k/HTisMpC.jpg" alt="HTisMpC" border="0">
        </div>
      </div>

      <div class="panel-group col-sm-6 col-sm-offset-3" id="accordion" role="tablist" aria-multiselectable="true">
        <div class="panel panel-default">
          <div class="panel-heading" role="tab" id="headingOne">
            <h4 class="panel-title">
              <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                <h1 class="app-name">Brand-X</h1>
              </a>
            </h4>
          </div>
          <div id="collapseOne" class="panel-collapse collapse in" role="tabpanel" aria-labelledby="headingOne">
            <div class="panel-body">
              <a target="_blank" href="http://www.brandxcavating.com"><img class="img-rounded" src="http://image.ibb.co/mEYtwQ/Screen_Shot_2017_04_14_at_9_29_51_PM.png" alt="Screen_Shot_2017_04_14_at_9_29_51_PM" border="0"></a>
            </div>
          </div>
        </div>
        <div class="panel panel-default">
          <div class="panel-heading" role="tab" id="headingTwo">
            <h4 class="panel-title">
              <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                <h1 class="app-name">NBA Trade Machine</h1>
              </a>
            </h4>
          </div>
          <div id="collapseTwo" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwo">
            <div class="panel-body">
              <a target="_blank" href="http://trade-machine.herokuapp.com"><img class="img-rounded" src="http://image.ibb.co/hEoRGQ/Screen_Shot_2017_04_14_at_9_32_59_PM.png" alt="Screen_Shot_2017_04_14_at_9_32_59_PM" border="0"></a>
            </div>
          </div>
        </div>
        <div class="panel panel-default">
          <div class="panel-heading" role="tab" id="headingThree">
            <h4 class="panel-title">
              <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                <h1 class="app-name">TeleVuesion</h1>
              </a>
            </h4>
          </div>
          <div id="collapseThree" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingThree">
            <div class="panel-body">
              <a target="_blank" href="http://tvue.herokuapp.com"><img class="img-rounded" src="http://image.ibb.co/mUCWi5/Screen_Shot_2017_04_14_at_9_35_44_PM.png" alt="Screen_Shot_2017_04_14_at_9_35_44_PM" border="0"></a>
            </div>
          </div>
        </div>
        <div class="panel panel-default">
          <div class="panel-heading" role="tab" id="headingFour">
            <h4 class="panel-title">
              <a class="collapsed" role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFour" aria-expanded="false" aria-controls="collapseFour">
                <h1 class="app-name">Affirmation</h1>
              </a>
            </h4>
          </div>
          <div id="collapseFour" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFour">
            <div class="panel-body">
              <a target="_blank" href="https://github.com/HRR20-Lotus/affirmation.io"><img class="img-rounded" src="http://image.ibb.co/kQv935/Screen_Shot_2017_04_14_at_11_55_27_PM.png" alt="Screen_Shot_2017_04_14_at_11_55_27_PM" border="0"></a>
            </div>
          </div>
        </div>
      </div>

      <div class="row">
        <div class="col-sm-6 col-sm-offset-3 text-center">
          <h3>Credits</h3>
          <div class="jumbotron">
            This site was built with Vue, Node && Express.<br>
            Thanks to Bootstrap, Canva && ImgBB for the visuals!
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'home',
    components: {},
    data() {
      return {
        guess: '',
        name: '',
        email: '',
        subject: '',
        message: '',
        joke: ''
      }
    },
    methods : {
      contactMe: function() {
        let data = {
          'Name': this.name,
          'Email': this.email,
          'Subject': this.subject,
          'Message': this.message
        };
        let firstName = this.name.split(' ')[0];
        let lastName = this.name.split(' ')[1];
        // Email
        this.$http.post('http://formspree.io/rajdesai94@gmail.com', data).then(response => {
          this.resetFields();
          // Jokes
          this.$http.get(`http://api.icndb.com/jokes/random?firstName=${firstName}&amp;lastName=${lastName}`, data).then(res => {
            console.log('Joke!', res.body);
            // this.joke = res.body.value.joke // Modal??
            this.message = res.body.value.joke
          }, res => {
            console.log('ERROR:', res);
          });
        }, response => {
          console.log('ERROR:', response);
        });
      },
      resetFields: function() {
        this.name = ''
        this.email = ''
        this.subject = ''
        this.message = ''
      },
      guessedRight: function() {
        return this.guess === "," || this.guess === "comma"
      }
    }
  }
</script>

<style>
body {
  background-color: #353558;
  color: #f1f4ff;
  overflow-x: hidden;
  position: relative;
  font-family: 'Open Sans', sans-serif;
}

img {
  width: 100%;
}

.list-group-item {
  background-color: transparent;
  color: #f1f4ff;
  border-color: #353558;
  transition: .3s ease-out;
  font-size: 1.25em;
}
.list-group-item:hover {
  background-color: #1f1f34;
}
.list-group-item:hover .link {
  color: #f1f4ff;
}
/*.list-group-item:hover .link {
  transform: translateX(10px);
}*/
a:hover {
  text-decoration: none;
}

.link {
  text-decoration: none;
  color: #353558;
  transition: .3s ease-out;
}

.side {
  position: fixed;
}

form {
  padding: 5px;
}
input, textarea {
  width: 100%;
  color: #E7E8E8;
  background-color: transparent;
  border-radius: 6px 6px 8px 8px;
  padding: 5px;
  border: 1px solid #f1f4ff;
  transition: .3s ease-out;
}
input:hover, textarea:hover {
  border-color: #1f1f34;
  color: #f1f4ff;
}
input:focus, textarea:focus {
  border: 1px solid #1f1f34;
  box-shadow: 0px 2px 1px 0px #1f1f34;
  outline: none;
}

.well {
  background-color: transparent;
  transition: .3s ease-out;
}
.well:hover {
  /*background-color: #f1f4ff;*/
  background-color: #1f1f34;
  border: 1px solid #1f1f34;
  cursor: pointer;
}
.glyphicon-send {
  color: #63D297;
  transition: .3s ease-out;
}
.glyphicon-send:hover {
  transform: translateX(3px) translateY(-3px);
}
.glyphicon-trash {
  color: #EE3017;
  transition: .3s ease-out;
}
.glyphicon-trash:hover {
  transform: translateY(3px);
}

.navbar {
  background-color: transparent;
  z-index: 10;
  border: none;
}
.logo {
  background-color: #353558;
  /*border-bottom: 1px solid #1f1f34;*/
  box-shadow: 0 1px 2px #1f1f34;
}

.apps {
  transition: .3s ease-out;
  margin-top: 4%;
  overflow-x: hidden;
}

.panel {
  border: none;
  background-color: #fff;
}
.panel .panel-heading {
  color: #f1f4ff;
  background-color: #353558;
  transition: .3s ease-out;
}
.panel .panel-collapse {
  background-color: #353558;
  /*border: 1px solid #1f1f34;*/
}
.panel:hover .panel-heading {
  background-color: #1f1f34;
}

.jumbotron {
  background: transparent;
}
/*.app {
  border: 1px solid #1f1f34;
}*/
.app-name {
  font-family: 'Pacifico', sans-serif;
}

</style>
