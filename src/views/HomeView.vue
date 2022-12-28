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
        <h1 class="button__heading">(button multi-sized)</h1>
        <ul>
          <li class="button__variant">
            <ul class="button__size-list">
              <li class="button__size-variant">
                <p class="button__title button__size-title">mobile</p> 
                <button-component
                  @click="clickBtn"
                  :disabled="false"
                  :primary="true"
                  width="100"
                  title=""
                >
                </button-component>
              </li>
              <li class="button__size-variant">
                <p class="button__title button__size-title">desktop</p> 
                <button-component
                  @click="clickBtn"
                  :disabled="false"
                  :primary="true"
                  title=""
                >
                </button-component>
              </li>
            </ul>
            
          </li>

          
        </ul>
      </div>

      <div class="contain__button">
        <h1 class="button__heading">(button timer)</h1>
        
      </div>

      <div class="contain__button">
        <h1 class="button__heading">(BUTTON CLASSIC)</h1>
        <ul>
          <li class="button__variant">
            <p class="button__title">(PRIMARY)</p> 
            <button-component
              @click="clickBtn"
              :disabled="false"
              :primary="true"
            >
            </button-component>
          </li>

          <li class="button__variant">
            <p class="button__title">(secondary)</p> 
            <button-component
              @click="clickBtn"
              :disabled="false"
              :secondary="true"
            >
            </button-component>
          </li>

          <li class="button__variant">
            <p class="button__title">(warning)</p> 
            <button-component
              @click="clickBtn"
              :disabled="false"
              :warning="true"
            >
            </button-component>
          </li>

          <li class="button__variant">
            <p class="button__title">(disabled)</p> 
            <button-component
              @click="clickBtn"
              :disabled="true"
            >
            </button-component>
          </li>

          <li class="button__variant">
            <p class="button__title">(info)</p> 
            <button-component
              @click="clickBtn"
              :disabled="false"
              :info="true"
            >
            </button-component>
          </li>

          <li class="button__variant">
            <p class="button__title">(danger)</p> 
            <button-component
              @click="clickBtn"
              :disabled="false"
              :danger="true"
            >
            </button-component>
          </li>

          <li class="button__variant">
            <p class="button__title">(action)</p> 
            <button-component
              @click="clickBtn"
              :disabled="false"
              :action="true"
            >
            </button-component>
          </li>
        </ul>
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
  justify-content: center;
  align-items: baseline;
  margin: 50px 0;
  padding: 72px 95px;
  border: 8px solid var(--white);
}

.contain__button {
  text-align: center;
}

.contain__button:not(:last-child) {
  padding-right: 107px;
}

.button__heading {
  padding-bottom: 18px;
  text-align: center;
  font-weight: 400;
  font-size: 18px;
  line-height: 24px;
  color: var(--title);
}

.button__variant {
  padding-bottom: 24px;
}

.button__size-list {
  display: flex;
}

.button__size-variant:not(:last-child) {
  padding-right: 24px;
}

.button__title {
  padding-bottom: 8px;
  text-align: left;
}
</style>

