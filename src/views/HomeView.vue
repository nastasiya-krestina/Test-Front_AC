<script>
import ButtonComponent from '../components/ButtonComponent.vue';

export default {
  components: {
    ButtonComponent,
  }, 

  data() {
    return {}
  },

  methods: {
    clickBtn() {
      console.log('Button clicked')
    }
  }
}
</script>

<template>
  <div class="container">
    <div class="contain">
      <div class="contain__button">
        <h1 class="button_heading">(BUTTON CLASSIC)</h1>
        <div class="button__variant">
          <p class="button_title">(PRIMARY)</p> 
          <button-component
            @click="clickBtn"
            :disabled="false"
            :primary="true"
          >
          </button-component>
        </div>
        
        <div class="button__variant">
          <p class="button_title">(secondary)</p> 
          <button-component
            @click="clickBtn"
            :disabled="false"
            :secondary="true"
          >
          </button-component>
        </div>

        <div class="button__variant">
          <p class="button_title">(warning)</p> 
          <button-component
            @click="clickBtn"
            :disabled="false"
            :warning="true"
          >
          </button-component>
        </div>

        <div class="button__variant">
          <p class="button_title">(disabled)</p> 
          <button-component
            @click="clickBtn"
            :disabled="true"
          >
          </button-component>
        </div>

        <div class="button__variant">
            <p class="button_title">(info)</p> 
            <button-component
              @click="clickBtn"
              :disabled="false"
              :info="true"
            >
            </button-component>
          </div>

        <div class="button__variant">
          <p class="button_title">(danger)</p> 
          <button-component
            @click="clickBtn"
            :disabled="false"
            :danger="true"
          >
          </button-component>
        </div>

        <div class="button__variant">
          <p class="button_title">(action)</p> 
          <button-component
            @click="clickBtn"
            :disabled="false"
            :action="true"
          >
          </button-component>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.container {
  margin: 0 auto;
  max-width: 1548px;
}

.contain {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: baseline;
  margin: 50px 0;
  padding: 72px 95px;
  border: 8px solid var(--white);
}

.contain__button {
  text-align: center;
}

.button_heading {
  padding-bottom: 18px;
  text-align: center;
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
  color: var(--disabled);
}

.button__variant {
  padding-bottom: 24px;
}

.button_title {
  padding-bottom: 8px;
  text-align: left;
}
</style>

