<template>
    <div class='container'>
        <navbar></navbar>
        <br>
        <transition name="fade">
          <faq v-if='showFAQ' :class="{'animated fadeInDown':showFAQ}"></faq>
        </transition>
        <transition name="fade">
          <contactdetails
            v-if='showContactDetails'
            :class="{'animated fadeInDown':showContactDetails}"
          >
          </contactdetails>
        </transition>
        <transition name="fade">
          <feesguidelines
            v-if='showFeeGuidelines'
            :class="{'animated fadeInDown':showFeeGuidelines}">
          </feesguidelines>
        </transition>
        <transition name="fade">
          <offersandprocedures
            v-if='showMainInterest'
            :class="{'animated fadeInDown':showMainInterest}">
          </offersandprocedures>
        </transition>
        <transition name="fade">
          <gynaecology v-if='showGynaecology' :class="{'animated fadeInDown':showGynaecology}">
          </gynaecology>
        </transition>
        <transition name="active">
          <obstetrics v-if='showObstetrics' :class="{'animated fadeInDown':showObstetrics}">
          </obstetrics>
        </transition>
        <transition name="fade">
          <aboutme v-if='showAboutMe' :class="{'animated fadeInDown':showAboutMe}"></aboutme>
        </transition>
        <!-- <reviewsandtestimonials></reviewsandtestimonials> -->
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
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
      this.showAboutMe = true;
    },
    obstetrics() {
      this.showAboutMe = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
      this.showObstetrics = true;
    },
    gynaecology() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
      this.showGynaecology = true;
    },
    maininterest() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showFeeGuidelines = false;
      this.showContactDetails = false;
      this.showFAQ = false;
      this.showMainInterest = true;
    },
    feeguidelines() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showContactDetails = false;
      this.showFAQ = false;
      this.showFeeGuidelines = true;
    },
    contactdetails() {
      this.showAboutMe = false;
      this.showObstetrics = false;
      this.showGynaecology = false;
      this.showMainInterest = false;
      this.showFeeGuidelines = false;
      this.showFAQ = false;
      this.showContactDetails = true;
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
