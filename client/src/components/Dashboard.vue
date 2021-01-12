<template>
    <div class='container'>
        <navbar></navbar>
        <br>
        <transition name="fade">
          <aboutme v-show='showAboutMe' :class="{'active':show}"></aboutme>
        </transition>
        <transition name="fade">
          <obstetrics v-show='showObstetrics' :class="{'active':show}"></obstetrics>
        </transition>
        <transition name="fade">
          <gynaecology v-show='showGynaecology' :class="{'active':show}"></gynaecology>
        </transition>
        <transition name="fade">
          <offersandprocedures v-show='showMainInterest' :class="{'active':show}">
          </offersandprocedures>
        </transition>
        <transition name="fade">
          <feesguidelines v-show='showFeeGuidelines' :class="{'active':show}"></feesguidelines>
        </transition>
        <!-- <reviewsandtestimonials></reviewsandtestimonials> -->
        <transition name="fade">
          <contactdetails v-show='showContactDetails' :class="{'active':show}"></contactdetails>
        </transition>
        <transition name="fade">
          <faq v-show='showFAQ' :class="{'active':show}"></faq>
        </transition>
        <div class="row">
          <div class="col-6">
            <directions></directions>
          </div>
          <div class="col-6">

          </div>
        </div>
    </div>
</template>

<script>
// import axios from 'axios';
import Navbar from './Navbar.vue';
import AboutMe from './AboutMe.vue';
import Obstetrics from './Obstetrics.vue';
import Gynaecology from './Gynaecology.vue';
import OffersAndProcedures from './OffersAndProcedures.vue';
import FeesGuidelines from './FeeGuidelines.vue';
import Directions from './Directions.vue';
// import ReviewsAndTestimonials from './ReviewsAndTestimonials.vue';
import ContactDetails from './ContactDetails.vue';
import FAQ from './FAQ.vue';

require('../assets/styles/custom.css');

export default {
  name: 'Dashboard',
  data() {
    return {
      showAboutMe: false,
      showObstetrics: false,
      showGynaecology: false,
      showMainInterest: false,
      showFeeGuidelines: false,
      showContactDetails: false,
      showFAQ: false,
    };
  },
  components: {
    navbar: Navbar,
    aboutme: AboutMe,
    obstetrics: Obstetrics,
    gynaecology: Gynaecology,
    offersandprocedures: OffersAndProcedures,
    feesguidelines: FeesGuidelines,
    directions: Directions,
    // reviewsandtestimonials: ReviewsAndTestimonials,
    contactdetails: ContactDetails,
    faq: FAQ,
  },
  methods: {
    aboutme() {
      this.showAboutMe = true;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
    },
    obstetrics() {
      this.showAboutMe = false;
      this.showObstetrics = true;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
    },
    gynaecology() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = true;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
    },
    maininterest() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = true;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
    },
    feeguidelines() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = true;
      this.showContactDetails = false;
      this.showFAQ = false;
    },
    contactdetails() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = true;
      this.showFAQ = false;
    },
    faq() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = true;
    },
    clear() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
    },
  },
  created() {
    this.$root.$on('click', (text) => {
      const screens = {
        aboutme: this.aboutme,
        obstetrics: this.obstetrics,
        gynaecology: this.gynaecology,
        maininterest: this.maininterest,
        feeguidelines: this.feeguidelines,
        contactdetails: this.contactdetails,
        faq: this.faq,
        clear: this.clear,
      };
      screens[text]();
      return {};
    });
  },
};
</script>
