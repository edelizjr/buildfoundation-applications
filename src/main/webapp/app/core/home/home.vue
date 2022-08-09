<template>
  <div class="home row">
    <div class="col"></div>
    <div class="col-md-8">
      <div>
        <b-card
          overlay
          img-src="https://picsum.photos/900/250/?image=3"
          img-alt="Card Image"
          text-variant="white"
          title="Image Overlay"
          sub-title="Subtitle"
        >
          <b-card-text> Some quick example text to build on the card and make up the bulk of the card's content. </b-card-text>
        </b-card>
      </div>

      <div>
        <b-carousel id="carousel-fade" style="text-shadow: 0px 0px 2px #000" fade indicators img-width="1024" img-height="480">
          <b-carousel-slide caption="First Slide" img-src="https://picsum.photos/1024/480/?image=10"></b-carousel-slide>
          <b-carousel-slide caption="Second Slide" img-src="https://picsum.photos/1024/480/?image=12"></b-carousel-slide>
          <b-carousel-slide caption="Third Slide" img-src="https://picsum.photos/1024/480/?image=22"></b-carousel-slide>
        </b-carousel>
      </div>

      <div>
        <b-card-group deck>
          <b-card title="Title" img-src="https://picsum.photos/300/300/?image=41" img-alt="Image" img-top>
            <b-card-text>
              This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit
              longer.
            </b-card-text>
            <template #footer>
              <small class="text-muted">Last updated 3 mins ago</small>
            </template>
          </b-card>

          <b-card title="Title" img-src="https://picsum.photos/300/300/?image=41" img-alt="Image" img-top>
            <b-card-text> This card has supporting text below as a natural lead-in to additional content. </b-card-text>
            <template #footer>
              <small class="text-muted">Last updated 3 mins ago</small>
            </template>
          </b-card>

          <b-card title="Title" img-src="https://picsum.photos/300/300/?image=41" img-alt="Image" img-top>
            <b-card-text>
              This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content
              than the first to show that equal height action.
            </b-card-text>
            <template #footer>
              <small class="text-muted">Last updated 3 mins ago</small>
            </template>
          </b-card>
        </b-card-group>
      </div>

      <div>
        <b-card-group columns>
          <b-card title="Card title that wraps to a new line" img-src="https://placekitten.com/g/400/450" img-alt="Image" img-top>
            <b-card-text>
              This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit
              longer.
            </b-card-text>
          </b-card>

          <b-card header="Quote">
            <blockquote class="blockquote mb-0">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
              <footer class="blockquote-footer">Someone famous in <cite title="Source Title">Source Title</cite></footer>
            </blockquote>
          </b-card>

          <b-card title="Title" img-src="https://placekitten.com/500/350" img-alt="Image" img-top>
            <b-card-text> This card has supporting text below as a natural lead-in to additional content. </b-card-text>
            <b-card-text class="small text-muted">Last updated 3 mins ago</b-card-text>
          </b-card>

          <b-card bg-variant="primary" text-variant="white">
            <blockquote class="card-blockquote">
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.</p>
              <footer>
                <small>Someone famous in <cite title="Source Title">Source Title</cite></small>
              </footer>
            </blockquote>
          </b-card>

          <b-card>
            <b-card-title>Title</b-card-title>
            <b-card-text> This card has supporting text below as a natural lead-in to additional content. </b-card-text>
            <b-card-text class="small text-muted">Last updated 3 mins ago</b-card-text>
          </b-card>

          <b-card img-src="https://picsum.photos/400/400/?image=41" img-alt="Image" overlay></b-card>

          <b-card img-src="https://picsum.photos/400/200/?image=41" img-alt="Image" img-top>
            <b-card-text>
              This is a wider card with supporting text below as a natural lead-in to additional content. This card has even longer content
              than the first.
            </b-card-text>
            <template #footer>
              <small class="text-muted">Footer Text</small>
            </template>
          </b-card>
        </b-card-group>
      </div>

      <div>
        <div class="alert alert-success" v-if="authenticated">
          <span v-if="username" v-text="$t('home.logged.message', { username: username })">You are logged in as user "{{ username }}"</span>
        </div>

        <div class="alert alert-warning" v-if="!authenticated">
          <span v-text="$t('global.messages.info.authenticated.prefix')">If you want to </span>
          <a class="alert-link" v-on:click="openLogin()" v-text="$t('global.messages.info.authenticated.link')">sign in</a
          ><span v-html="$t('global.messages.info.authenticated.suffix')"
            >, you can try the default accounts:<br />- Administrator (login="admin" and password="admin") <br />- User (login="user" and
            password="user").</span
          >
        </div>
      </div>
    </div>
    <div class="col"></div>
  </div>
</template>

<script lang="ts" src="./home.component.ts"></script>
