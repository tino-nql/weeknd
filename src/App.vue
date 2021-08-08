<template>
  <div class="wrapper">
    <div ref="home" class="header">
      <div class="container-xl">
        <div>
          <b-navbar toggleable="lg" type="light" variant="faded">

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
              <!-- Right aligned nav items -->
              <b-navbar-nav></b-navbar-nav>
              <b-navbar-nav class="ml-auto options">
                <b-nav-item @click.prevent="scrollMeTo('home')">HOME</b-nav-item>
                <b-nav-item @click.prevent="scrollMeTo('photos')">PHOTOS</b-nav-item>
                <b-nav-item @click.prevent="scrollMeTo('bio')">BIO</b-nav-item>
                <b-nav-item @click.prevent="scrollMeTo('media')">MEDIA</b-nav-item>
                <b-nav-item @click.prevent="scrollMeTo('contact')">CONTACT</b-nav-item>
              </b-navbar-nav>
            </b-collapse>
          </b-navbar>
        </div>
        <div class="title">
          <img class="logo" src="./assets/typo-01.png">
        </div>
      </div>
    </div>
    <div>
      <div class="bg-1">
        <div class="main-content container-xl text-white pt-5">
          <div class="d-inline-block mb-5">
            <div class="float-left mr-4">
              <h1 style="font-size: 4rem;">Cuối tuần</h1>
              <h3 style="font-size: 2rem;">WXRDIE ft. KayC & 2pillz</h3>
            </div>
            <div class="float-left mt-4">
              <b-button variant="outline-warning"><a href="https://youtu.be/5T3ip8yQp_k" target="_blank" rel="noopener" class="text-warning">LISTEN HERE</a></b-button>
            </div>
          </div>
          <div class="d-inline-block">
            <div class="video-container mr-4 mb-4">
              <iframe width="100%" height="100%" src="https://www.youtube.com/embed/VwdLugyKkWs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
            <h5 class="w-100">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eius minus quos quas excepturi fuga tempore voluptates maxime qui corporis! Voluptate quia quibusdam debitis incidunt dicta et accusamus sunt voluptas neque.</h5>
          </div>
        </div>
      </div>
      <div class="bg-3">
        <div ref="photos" class="collections container-xl pt-5">
          <div class="title-line">Photos</div>
          <div class="container-xl mt-5">
            <div class="row">
              <div class="col-sm">
                <img src="./assets/Untitled-1-04.jpg" width="100%">
                <img class="mt-4" src="./assets/Untitled-1-06.jpg" width="100%">
                <img class="mt-4" src="./assets/Untitled-1-07.jpg" width="100%">
              </div>
              <div class="col-sm">
                <img src="./assets/Untitled-1-01.jpg" width="100%">
                <img class="mt-4" src="./assets/Untitled-1-09.jpg" width="100%">
                <img class="mt-4" src="./assets/Untitled-1-09.jpg" width="100%">
                <img class="mt-4" src="./assets/Untitled-1-02.jpg" width="100%">
              </div>
              <div class="col-sm">
                <img src="./assets/Untitled-1-03.jpg" width="100%">
                <img class="mt-4" src="./assets/Untitled-1-05.jpg" width="100%">
                <img class="mt-4" src="./assets/Untitled-1-08.jpg" width="100%">
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="bg-4">
        <div ref="bio" class="bio container-xl pt-5">
          <div class="title-line">BIO</div>
          <div class="text-white mt-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa dolorem illum rem doloribus magnam? Libero facere sed architecto, totam officia velit amet a, inventore voluptatibus animi quos sint earum ad nisi in nemo error reiciendis placeat, dicta autem! Alias voluptatibus voluptatem repellendus vel ut maxime libero veritatis ea deleniti sint. Voluptas illo fuga dolore, tempora porro, maiores nihil dignissimos odio, dolor rerum inventore hic illum. Quibusdam deserunt eos eaque, corporis culpa numquam labore ratione eligendi dolorum vero vitae id commodi, beatae eius nesciunt repellat ipsa. Laborum deserunt illo excepturi natus. Blanditiis necessitatibus possimus nobis? Commodi libero esse, totam eius, nisi cumque aliquid recusandae necessitatibus nam illum eligendi iste ab incidunt, quasi enim laborum. Ex, tenetur! Voluptate iusto quis quas ipsa magnam modi, sequi non reprehenderit. Voluptatum quod, voluptates praesentium quidem rerum exercitationem aut veritatis quia dolorem rem nisi, dolorum, est porro vel! Voluptate laborum esse provident nam, autem porro nisi commodi dolor minima exercitationem, tempora quibusdam suscipit neque recusandae, quia distinctio! Dicta, perspiciatis. Ea animi quam cum reprehenderit velit similique veritatis maxime, consequuntur, sed voluptatibus adipisci at quos consectetur officia? Impedit enim natus consequuntur atque eaque repudiandae voluptatum corporis quidem, consectetur culpa, laudantium eum voluptatem amet molestiae sint totam numquam.</div>
        </div>
        <div ref="media" class="media-container container-xl pt-5">
          <div class="title-line">MEDIA</div>
          <div class="mt-5 text-white">GIGS / INTERVIEWS:<br>info@wxrdiemusic.com</div>
        </div>
      </div>
      <div class="bg-5">
        <div ref="contact" class="contact container-xl pt-5">
          <div class="title-line">CONTACT</div>
          <div class="mt-5 text-white">
            <b-form @submit.prevent="submitContactForm" class="contact-form">
              <b-form-group
                id="input-name"
                label="Name:"
                label-for="input-name"
              >
                <b-form-input
                  id="input-name"
                  v-model="form.name"
                  type="text"
                  placeholder="Your fullname"
                  required
                ></b-form-input>
              </b-form-group>
              <b-form-group
                id="input-email"
                label="Email:"
                label-for="input-email"
              >
                <b-form-input
                  id="input-email"
                  v-model="form.email"
                  type="email"
                  placeholder="Your email"
                  required
                ></b-form-input>
              </b-form-group>
              <b-form-group
                id="input-message"
                label="Message:"
                label-for="input-message"
              >
                <b-form-textarea
                  id="input-message"
                  v-model="form.message"
                  type="text"
                  placeholder="Leave your message here"
                  rows="6"
                  required
                ></b-form-textarea>
              </b-form-group>
              <b-button type="submit" variant="outline-warning">Submit</b-button>
            </b-form>
          </div>
        </div>
        <div class="info text-white d-flex justify-content-center align-center">
          <div class="text-center">
            <div style="font-size: 0.75rem;">BE THE FIRST TO HEAR THE LATEST NEWS</div>
            <b-form inline @submit.prevent="signUp()" class="signup-form">
              <b-form-group
                id="input-signup"
                class="float-left"
              >
                <b-form-input
                  id="input-signup"
                  v-model="form.signup"
                  type="email"
                  required
                ></b-form-input>
              </b-form-group>
              <b-button type="submit" class="ml-2" variant="outline-warning">SIGN UP</b-button>
            </b-form>
          </div>
        </div>
        <div class="quote text-center text-white">
          “Made in Donglaos, revamped in Donglaos”
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      form: {
        name: '',
        email: '',
        message: '',
        signup: ''
      }
    }
  },
  methods: {
    scrollMeTo (refName) {
      var element = this.$refs[refName]
      var top = element.offsetTop

      window.scrollTo(0, top)
    },
    submitContactForm () {
      if (!this.form.name || !this.form.email || !this.form.message) {
        return
      }
      const payload = new FormData()

      payload.append('name', this.form.name)
      payload.append('email', this.form.email)
      payload.append('message', this.form.message)
      this.$http.post('https://script.google.com/macros/s/AKfycbxQwouseI7YyfP4NgdV8BKmqSq6nuxJJ-U2Tl3Nk8E2umxDG2f1xahAOGvVqKtHwss/exec', payload).then(body => {
        if (!body.data || body.data.result !== 'success') {
          alert('Failed to submit form! Try later')
          return
        }

        this.form = {
          name: '',
          email: '',
          message: '',
          signup: ''
        }
        alert('Submit successfully!')
      })
    },
    signUp () {
      if (!this.form.signup) {
        return
      }

      const payload = new FormData()
      payload.append('email', this.form.signup)
      this.$http.post('https://script.google.com/macros/s/AKfycbyDGcXPzOgCUjc1LH_JdUj3Dd8QKH1fPWXWC9xkM0mGZhI6hiU3-DrTcMeji1BNshQ/exec', payload).then(body => {
        if (!body.data || body.data.result !== 'success') {
          alert('Failed to submit form! Try later')
          return
        }

        this.form = {
          name: '',
          email: '',
          message: '',
          signup: ''
        }
        alert('Submit successfully!')
      })
    }
  }
}
</script>
<style lang="css">
@font-face {
  font-family: LexendMedium;
  src: url('./assets/fonts/Lexend-Medium.ttf');
}

@font-face {
  font-family: LexendRegular;
  src: url('./assets/fonts/Lexend-Regular.ttf');
}

@font-face {
  font-family: COPRGTB;
  src: url('./assets/fonts/COPRGTB.TTF');
}

@import '~bootstrap/dist/css/bootstrap.min.css';
@media (max-width: 575.98px) {
  .logo {
    width: 100%;
  }
  .video-container {
    width: 100%;
    height: 210px;
  }

  .form-inline {
    display: block !important;
  }
}
@media (min-width: 576px) {
  .video-container {
    width: 100%;
    height: 500px;
  }
  .contact-form {
    width: 100%;
  }
  .logo {
    width: 100%;
  }
  .form-inline {
    display: block !important;
  }
  .bg-1 .bg-3 .bg-4 .bg-5 {
    visibility: hidden;
  }
}

@media (min-width: 768px) {
  .video-container {
    float: left;
    width: 60%;
    height: 500px;
  }
  .contact-form {
    width: 100%;
  }
  .logo {
    width: 500px;
  }
  .bg-1 .bg-3 .bg-4 .bg-5 {
    background-size: cover 100%;
  }
}

@media (min-width: 992px) {
  .video-container {
    float: left;
    width: 50%;
    height: 500px;
  }

  .contact-form {
    width: 70%;
  }
  .logo {
    width: 600px;
  }
}

@media (min-width: 1200px) {
  .container-xl {
    max-width: 2000px !important;
    padding-left: 30px !important;
    padding-right: 30px !important;
  }
  .video-container {
    float: left;
    width: 1000px;
    height: 500px;
  }

  .contact-form {
    width: 800px;
  }
  .logo {
    width: 1000px;
  }
}

html {
  scroll-behavior: smooth;
}

html body {
  margin: 0;
  font-family: LexendRegular;
}

.header {
  overflow: hidden;
  position: relative;
  padding: 0 24px;
  background-image:
  /* top, transparent red */
  linear-gradient(
    rgba(75, 179, 27, 0.45),
    rgba(75, 179, 27, 0.45)
  ),
  /* your image */
  url('../src/assets/LBOO0362.jpg');
  background-size: cover;
  background-position: top left;
  background-repeat: no-repeat;
}

.options a {
  color: #fff !important;
}

.main-container {
  z-index: 9999;
}
.bg-1 {
  background-image:
  /* top, transparent red */
  linear-gradient(
    #146326e0,
    #146326e0
  ),
  /* your image */
  url('../src/assets/LBOO9889.jpg');
  background-size: cover;
  background-position: top;
  background-repeat: no-repeat;
}

.bg-3 {
  background-image:
  /* top, transparent red */
  linear-gradient(
    #146326e0,
    #146326e0
  ),
  /* your image */
  url('../src/assets/LBOO9997.jpg');
  background-size: cover;
  background-position: top;
  background-repeat: no-repeat;
}
.bg-4 {
  background-image:
  /* top, transparent red */
  linear-gradient(
    #146326e0,
    #146326e0
  ),
  /* your image */
  url('../src/assets/LBOO9988.jpg');
  background-size: cover;
  background-position: top;
  background-repeat: no-repeat;
}
.bg-5 {
  background-image:
  /* top, transparent red */
  linear-gradient(
    #146326e0,
    #146326e0
  ),
  /* your image */
  url('../src/assets/LBOO0427.jpg');
  background-size: cover;
  background-position: top;
  background-repeat: no-repeat;
}

.title {
  font-size: 2rem;
  display: flex;
  vertical-align: middle;
  align-items: center;
  height: 450px;
}

.title-line {
  font-size: 2rem;
  font-weight: 400;
  color: #fff;
  display: flex;
  align-items: center;
  vertical-align: middle;
}

.title-line:before {
  content: "";
  display: block;
  margin-right: 20px;
  width: 130px;
  height: 2px;
  background: #f4bd22;
}

.contact-form {
  max-width: 100%;
}

.info {
  padding: 8em 0;
}

.main-content {
  padding: 0 30px 30px 24px;
}
.collections {
  padding: 0 24px 100px 24px;
}
.contact {
  padding: 0 24px 100px 24px;
}
.bio {
  padding: 0 24px;
}

.media-container {
  padding: 0 24px;
}
.quote {
  font-size: 1.5rem;
  padding-bottom: 100px;
}
</style>
