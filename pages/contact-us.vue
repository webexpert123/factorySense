<template>
  <div>
    <div class="getInTouch">
      <div class="getInTouchWhiteBox">
        <h2><span style="color: #ffa300;">GET IN TOUCH</span><br />WITH FACTORY SENSE</h2>
        <h3>WE’D LOVE TO HEAR FROM YOU!</h3>
        <p>Whether you’re interested in finding out more
          information about our products, seeking advice on how
          to optimise your production process, or just want to
          say hi - <strong style="color:#2b3d4f">we’d be delighted to hear from you.</strong></p>
      </div>
    </div>
    <div class="deliveringValue flex">
      <div class="deliveringValueBox w-50">
        <img src="~assets/images/talktosales.jpg" class="imgCenter" />
        <p class="talkToSales">Talk to Sales</p>
        <p class="talkContent">Interested in RFID solutions? Pick up the phone, email or
          fill out the form below to speak to one of our experts. </p>
        <ul>
          <li><a href="tel:+1972984-7176"><img src="~assets/images/tell.jpg" class="inline-block" /> +1 (972) 984-7176</a>
          </li>
          <li><a href="mailto:info@factorysense.io"><img src="~assets/images/email.jpg" class="inline-block" />
              info@factorysense.io</a></li>
        </ul>
      </div>
      <div class="deliveringValueBox w-50">
        <img src="~assets/images/support.jpg" class="imgCenter" />
        <p class="talkToSales">Contact Customer Support</p>
        <p class="supportContent">Need some help?<br />Our support team is available 24/7.</p>
        <ul>
          <li><a href="tel:+1972984-7176"><img src="~assets/images/tell.jpg" class="inline-block" /> +1 (972) 984-7176</a>
          </li>
          <li><a href="mailto:support@factorysense.io"><img src="~assets/images/email.jpg" class="inline-block" />
            support@factorysense.io</a></li>
        </ul>
      </div>
    </div>
    <div class="contactForm">
      <div class="container">
        <h3>Or if you prefer, fill out the form below and a member of our team will get back to you as soon as possible.
        </h3>
        <h3 v-if="submitted == true" style="color: green; padding-top: 5px;"> Email successfully sent</h3>
        <h3 v-if="emailError == true" style="color: red; padding-top: 5px;"> Email not sent</h3>
        <form @submit.prevent="handleSubmit">
          <div class="inputRow flex">
            <div class="flex-auto w-50 input-box">
              <input v-model="form.fName" type="text" placeholder="First name" required />
            </div>
            <div class="flex-auto w-50 input-box">
              <input v-model="form.lName" type="text" placeholder="Last name" required />
            </div>
          </div>
          <div class="inputRow flex">
            <div class="flex-auto w-50 input-box">
              <input v-model="form.email" type="email" placeholder="Email" required @blur=validateEmail() @input=checkEmail() />
              <p v-if="inputEmailError" class="text-red-500 text-sm">Invalid email</p>
            </div>
            <div class="flex-auto w-50 input-box">
              <input v-model="form.company" type="text" placeholder="Company" required />
            </div>
          </div>
          <div class="textareaRow">
            <textarea v-model="form.message" type="text" placeholder="Message" required />
          </div>
          <div class="formFooter">
            <button type="submit" class="formSubmit" :disabled=emailTrue>Send</button>
          </div>
        </form>
        
      </div>
    </div>
    <div class="contactMap">
      <div class="container text-center">
        <img src="~assets/images/build.png" class="relative mx-auto" />
        <p>2035 Central Circle, Suite 100, McKinney TX 75969, United States
          For Media Enquiries: <a href="mailto:media@factorysense.io">media@factorysense.io</a></p>
      </div>
    </div>
  </div>
</template>
  
<script>

export default {
  name: 'Contact',
  data() {
    return {
      form: {
        fName: "",
        lName: "",
        email: "",
        company: "",
        message: "",
      },
      submitted: false,
      emailError: false,
      emailTrue: true,
      inputEmailError: false
    };
  },
  methods: {
    checkEmail(){
      /* eslint-disable */
      const validRegex = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
      
      const res = validRegex.test(this.form.email);
      if(res) {
        this.emailTrue=false
        this.inputEmailError = false
      } else{
        this.emailTrue=true
      }
      /* eslint-enable */
    },
    validateEmail() {
      /* eslint-disable */
      const validRegex = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
      
      const res = validRegex.test(this.form.email);
      if(res) {
        this.emailTrue=false
        this.inputEmailError = false
      } else {
        this.inputEmailError = true
        this.emailTrue=true
      }
      /* eslint-enable */
    },
    async handleSubmit () {
      this.submitted = false
      this.emailError = false

      const formData = new FormData();

      formData.append('firstname', this.form.fName);
      formData.append('lastname', this.form.lName);
      formData.append('email', this.form.email);
      formData.append('company', this.form.company);
      formData.append('message', this.form.message);
      
      await fetch(`https://forms.hubspot.com/uploads/form/v2/23878667/37983118-92dd-49d7-920f-e00132cb810c`,{body: formData,method: "post"}).then((data)=>{
        this.submitted = true
        this.form = {
          fName: "",
          lName: "",
          email: "",
          company: "",
          message: "",
        }
      }).catch((err)=>{
        // eslint-disable-next-line no-console
        console.log('Error-', err)
        this.emailError = true
      });
    }
  }

}
</script>
<style>
.getInTouchWhiteBox {
  max-width: 640px;
  margin: 0 auto;
  text-align: center;
  padding: 40px;
  background: #fff;
  position: relative;
}

.getInTouch {
  background: url('~assets/images/contact-banner.jpg');
  padding: 50px 15px;
  border-top: solid 4px #ffa300;
  border-bottom: solid 4px #ffa300;
  position: relative;
  background-repeat: no-repeat;
  background-size: cover;
}

.getInTouch:before {
  content: "";
  background: #000;
  height: 100%;
  width: 100%;
  display: block;
  position: absolute;
  top: 0;
  bottom: 0;
  z-index: 0;
  left: 0;
  right: 0;
  opacity: 0.3;
}

.getInTouch h2 {
  font-size: 3.15rem;
  line-height: 1.2;
  font-weight: 700;
  border-bottom: dashed 2px #488efc;
  padding-bottom: 25px;
  margin-bottom: 25px;
  color: #2b3d4f;
}

.getInTouch h3 {
  font-size: 30px;
  font-weight: 700;
}

.getInTouch p {
  font-size: 20px;
  padding: 8px 30px;
}

.deliveringValue {
  max-width: 1200px;
  padding: 15px;
  margin: 0 auto;
  gap: 60px;
  position: relative;
  top: -45px;
}

.deliveringValueBox {
  background: #fffaf2;
  padding: 50px;
  text-align: center;
  box-shadow: 3px 5px 22px #00000045;
}

img.imgCenter {
  margin: 0 auto 20px auto;
}

p.talkToSales {
  font-weight: 600;
  font-size: 18px;
}

.deliveringValueBox p {
  font-size: 18px;
}

p.supportContent,
p.talkContent {
  padding: 20px;
}

.deliveringValueBox ul li a {
  font-size: 20px;
  color: #126efe;
  font-weight: 600;
}

.deliveringValueBox img.inline-block {
  padding-right: 5px;
}

.contactForm .container {
  max-width: 960px;
  margin: 0 auto;
  padding: 70px;
  text-align: center;
  box-shadow: 3px 5px 22px #00000045;
  z-index: 9;
  position: relative;
  border: solid 1px #126eff;
  background: #fff;
}

.inputRow input {
  width: 100%;
}

.textareaRow textarea {
  height: 120px;
  width: 100%;
  margin-top: 25px;
}

.inputRow {
  margin-top: 25px;
  gap: 40px;
}

select#country {
  width: 100%;
}

.w-50 {
  flex: 50%;
}

.contactForm h3 {
  font-size: 20px;
  color: #2b3d4f;
  font-weight: 700;
  max-width: 630px;
  margin: 0 auto;
}

button.formSubmit {
  background: #126eff;
  padding: 12px 60px;
  color: #fff;
  font-weight: 600;
  font-size: 20px;
  border-radius: 10px;
  margin-top: 30px;
}

.contactForm input,
.contactForm textarea,
.contactForm select {
  border-color: #ffa300;
  padding: 12px;
}

.contactMap {
  position: relative;
  top: -30px;
}

.contactMap .container {
  max-width: 1400px;
  margin: 0 auto;
  background: url(~assets/images/GoogleMapTA.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  padding: 70px 15px 40px 15px;
}

.contactMap .container:before {
  content: "";
  background: #ffa300;
  height: 100%;
  width: 100%;
  display: block;
  position: absolute;
  top: 0;
  bottom: 0;
  z-index: 0;
  left: 0;
  right: 0;
  opacity: 0.9;
}

.contactMap p {
  position: relative;
  max-width: 630px;
  margin: 0 auto;
  font-size: 20px;
  color: #fff;
  font-weight: 600;
}

.contactMap img {
  max-width: 56px;
  margin-bottom: 10px;
}

@media only screen and (max-width: 767px) {
  .getInTouch h2 {
    font-size: 2.15rem;
  }

  .getInTouch h3 {
    font-size: 21px;
  }

  .getInTouch p {
    font-size: 16px;
  }

  .contactForm {
    width: 95%;
    margin: auto;
  }
  .deliveringValueBox p {
    font-size: 16px;
  }

  .deliveringValueBox ul li a {
    font-size: 16px;
  }
  .contactMap p {
    font-size: 16px;
  }
  .contactForm h3 {
    font-size: 16px;
  }

  .deliveringValue {
    gap: 37px;
  }

  .contactMap .container{
    padding: 70px 50px 40px 50px;
  }
}

@media only screen and (max-width: 600px) {
  .inputRow {
    display: contents;
  }
  .deliveringValue {
    display: grid;
  }

  .contactForm .container {
    padding: 50px;
  }
  .input-box {
    padding-bottom: 15px;
  }
  .contactForm h3 {
    padding-bottom: 25px;
  }
}
</style>
