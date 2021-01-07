<template>
    <div class="container jumbotron">
        <a id="reviewsandtestimonials"><h2>Reviews and Testimonials</h2></a>
        <b-card>
            <b-media>
            <template #aside>
                <b-img blank blank-color="#ccc" width="64" alt="Dr Frohlich Picture"></b-img>
            </template>

            <h5 class="mt-0">Dr. Frohlich</h5>
            <p>
                Cras sit amet nibh libero, in gravida nulla. Nulla vel metus scelerisque
                ante sollicitudin.
                Cras purus odio, vestibulum in vulputate at, tempus viverra turpis. Fusce
                condimentum nunc
                ac nisi vulputate fringilla. Donec lacinia congue felis in faucibus.
            </p>
            <p>
                Donec sed odio dui. Nullam quis risus eget urna mollis ornare vel eu leo.
                Cum sociis natoque
                penatibus et magnis dis parturient montes, nascetur ridiculus mus.
            </p>
            </b-media>
        </b-card>
    </div>
</template>
<script>
export default {
  name: 'ReviewsAndTestimonials',
  props: ['message'],
};
</script>
