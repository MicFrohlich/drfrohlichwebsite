<template>
    <div class="container">
        <navbar></navbar>
        <br>
        <aboutme></aboutme>
        <obstetrics></obstetrics>
        <gynaecology></gynaecology>
        <offersandprocedures></offersandprocedures>
        <feesguidelines></feesguidelines>
        <directions></directions>
        <reviewsandtestimonials></reviewsandtestimonials>
        <contactdetails></contactdetails>
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
import ReviewsAndTestimonials from './ReviewsAndTestimonials.vue';
import ContactDetails from './ContactDetails.vue';

export default {
  name: 'Dashboard',
  data() {
    return {

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
    reviewsandtestimonials: ReviewsAndTestimonials,
    contactdetails: ContactDetails,
  },
  methods: {
  },
  created() {
  },
};
</script>
