<template>
  <div>
    <b-navbar toggleable='lg' type='dark' variant='info'>
        <b-navbar-brand @click='clear' v-show='showClear'>Dr. Emeric Frohlich</b-navbar-brand>
        <b-navbar-toggle target='nav-collapse'></b-navbar-toggle>
        <b-collapse id='nav-collapse' is-nav toggleable='xl'>
        <b-navbar-nav>
            <b-nav-item @click='aboutme' v-show='showAboutMe'>About Me</b-nav-item>
            <b-nav-item @click='obstetrics' v-show='showObstetrics'>
              Obstetrics
            </b-nav-item>
            <b-nav-item @click='gynaecology' v-show='showGynaecology'>
              Gynaecology
            </b-nav-item>
            <b-nav-item @click='maininterest' v-show='showMainInterest'>
              Main Interest
            </b-nav-item>
            <b-nav-item @click='feeguidelines' v-show='showFeeGuidelines'>
              Guideline to Fees
            </b-nav-item>
 <!-- <b-nav-item href='#reviewsandtestimonials'>Reviews and Testimonials</b-nav-item> -->
            <b-nav-item @click='contactdetails' v-show='showContactDetails'>
              Contact Details
            </b-nav-item>
            <b-nav-item @click='faq' v-show='showFAQ'>FAQ</b-nav-item>
        </b-navbar-nav>
        <!-- Right aligned nav items -->
        </b-collapse>
    </b-navbar>
    <div class='row'>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  props: ['is-nav'],
  data() {
    return {
      showAboutMe: true,
      showObstetrics: true,
      showGynaecology: true,
      showMainInterest: true,
      showFeeGuidelines: true,
      showContactDetails: true,
      showFAQ: true,
      showClear: true,
    };
  },
  methods: {
    aboutme() {
      this.$root.$emit('click', 'aboutme');
    },
    obstetrics() {
      this.$root.$emit('click', 'obstetrics');
    },
    gynaecology() {
      this.$root.$emit('click', 'gynaecology');
    },
    maininterest() {
      this.$root.$emit('click', 'maininterest');
    },
    feeguidelines() {
      this.$root.$emit('click', 'feeguidelines');
    },
    contactdetails() {
      this.$root.$emit('click', 'contactdetails');
    },
    faq() {
      this.$root.$emit('click', 'faq');
    },
    clear() {
      this.$root.$emit('click', 'clear');
    },
  },
};
</script>
