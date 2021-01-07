<template>
    <div class="container jumbotron">
        <div class="header">
            <a id="obstetrics">
                <h2>
                    Obstetrics:
                </h2>
            </a>
            <p>A week by week guide to your babies development</p>
        </div>
        <div>
            <!-- Carousel and Images -->
        <b-carousel
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        controls
        indicators
        background="#ababab"
        img-width="1024"
        img-height="480"
        style="text-shadow: 1px 1px 2px #333;"
        @sliding-start="onSlideStart"
        @sliding-end="onSlideEnd"
        >
        <!-- Text slides with image -->
        <b-carousel-slide
            caption="First Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=52"
        ></b-carousel-slide>

        <!-- Slides with custom text -->
        <b-carousel-slide
            caption="Second Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=54">
        </b-carousel-slide>

        <!-- Slides with image only -->
        <b-carousel-slide
            caption="Third Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=58">
        </b-carousel-slide>

        <b-carousel-slide
            caption="Fourth Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=58">
        </b-carousel-slide>

        <b-carousel-slide
            caption="Fifth Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=58">
        </b-carousel-slide>

        <b-carousel-slide
            caption="Sixth Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=58">
        </b-carousel-slide>

        <b-carousel-slide
            caption="Seventh Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=58">
        </b-carousel-slide>

        <b-carousel-slide
            caption="Eighth Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=58">
        </b-carousel-slide>

        <b-carousel-slide
            caption="Ninth Month"
            text="Whatever Text You Want"
            img-src="https://picsum.photos/1024/480/?image=58">
        </b-carousel-slide>
        <!-- Slide with blank fluid image to maintain slide aspect ratio -->
        <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
            <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros
            felis, tincidunt
            a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
            </p>
        </b-carousel-slide>
        </b-carousel>

        <p class="mt-4">
        Slide #: {{ slide }}<br>
        Sliding: {{ sliding }}
        </p>
            <!-- Carousel and Images -->
        <div class="header">
            <h3>The Normal Pregnancy Plan:</h3>
            <p>This was on the plan but i need the text</p>
        </div>
  </div>
    </div>
</template>
<script>
export default {
  name: 'Obstetrics',
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  methods: {
    onSlideStart(slide) {
      if (slide) {
        this.sliding = true;
      }
    },
    onSlideEnd(slide) {
      if (slide) {
        this.sliding = false;
      }
    },
  },
  props: ['message'],
};
</script>
