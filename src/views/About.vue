<template>
  <div class="about">
    <h1>This is an about page</h1>
    <BButton>Button</BButton>
    <BButton variant="danger">Button</BButton>
    <BButton variant="success">Button</BButton>
    <BButton variant="outline-primary">Button</BButton>
    <BButton id="tooltip-target-1">
      Hover Me
    </BButton>
    <BTooltip
      target="tooltip-target-1"
      triggers="hover">
      I am tooltip <b>component</b> content!
    </BTooltip>
    <br />
    <hr />
    <br />
    <BAlert
      v-model="showDismissibleAlert"
      variant="danger"
      dismissible>
      Dismissible Alert!
    </BAlert>

    <BAlert
      :show="dismissCountDown"
      dismissible
      variant="warning"
      @dismissed="dismissCountDown=0"
      @dismiss-count-down="countDownChanged">
      <p>This alert will dismiss after {{ dismissCountDown }} seconds...</p>
      <BProgress
        variant="warning"
        :max="dismissSecs"
        :value="dismissCountDown"
        height="4px"></BProgress>
    </BAlert>
    <BButton
      @click="showAlert"
      variant="info"
      class="m-1">
      Show alert with count-down timer
    </BButton>
    <br />
    <hr />
    <br />
    <div class="row">
      <div class="col-md">
        <BCard
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2">
          <BCardText>
            Some quick example text to build on the card title and make up the bulk of the card's content.
          </BCardText>

          <BButton href="#" variant="primary">Go somewhere</BButton>
        </BCard>
      </div>
      <div class="col-md">
        <BCard
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2">
          <BCardText>
            Some quick example text to build on the card title and make up the bulk of the card's content.
          </BCardText>

          <BButton href="#" variant="primary">Go somewhere</BButton>
        </BCard>
      </div>
      <div class="col-md">
        <BCard
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2">
          <BCardText>
            Some quick example text to build on the card title and make up the bulk of the card's content.
          </BCardText>

          <BButton href="#" variant="primary">Go somewhere</BButton>
        </BCard>
      </div>
      <div class="col-md">
        <BCard
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2">
          <BCardText>
            Some quick example text to build on the card title and make up the bulk of the card's content.
          </BCardText>

          <BButton href="#" variant="primary">Go somewhere</BButton>
        </BCard>
      </div>
      <div class="col-md">
        <BCard
          title="Card Title"
          img-src="https://picsum.photos/600/300/?image=25"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem;"
          class="mb-2">
          <BCardText>
            Some quick example text to build on the card title and make up the bulk of the card's content.
          </BCardText>

          <BButton href="#" variant="primary">Go somewhere</BButton>
        </BCard>
      </div>
    </div>

  </div>
</template>
<script>
export default {
  name: 'About',
  data () {
    return {
      dismissSecs: 10,
      dismissCountDown: 0,
      showDismissibleAlert: false
    }
  },
  methods: {
    countDownChanged (dismissCountDown) {
      this.dismissCountDown = dismissCountDown
    },
    showAlert () {
      this.dismissCountDown = this.dismissSecs
    }
  }
}
</script>
