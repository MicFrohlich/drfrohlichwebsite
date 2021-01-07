<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
        <b-navbar-brand href="#">Dr. Emeric Frohlich</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav toggleable='xl'>
        <b-navbar-nav>
            <b-nav-item href="#aboutme">About Me</b-nav-item>
            <b-nav-item href="#obstetrics">Obstetrics</b-nav-item>
            <b-nav-item href="#gynaecology">Gynaecology</b-nav-item>
            <b-nav-item href="#offersandprocedures">List of Procedures/Offers</b-nav-item>
            <b-nav-item href="#feeguidelines">Guideline to Fees</b-nav-item>
            <b-nav-item href="#directions">Directions</b-nav-item>
            <b-nav-item href="#reviewsandtestimonials">Reviews and Testimonials</b-nav-item>
            <b-nav-item href="#contactdetails">Contact Details</b-nav-item>
        </b-navbar-nav>
        <!-- Right aligned nav items -->
        </b-collapse>
    </b-navbar>
    <div class="row">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  props: ['is-nav'],
};
</script>
