<template>
  <div class="add-form">
    <div class="add-form__title">
      <input
        v-model="title"
        placeholder="Заголовок темы"
        type="text"
        name="title"
        id="title"
        autocomplete="off"
      />
    </div>
    <div class="add-form__text">
      <textarea v-model="text" placeholder="Опишите подробнее" name="text" id="text" rows="3"></textarea>
    </div>
    <div class="add-form__footer">
      <div v-if="title && text" @click="clear" class="add-form__footer-clear">
        <svg
          height="14"
          viewBox="0 0 365.696 365.696"
          fill="none"
          width="14"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="m243.1875 182.859375 113.132812-113.132813c12.5-12.5 12.5-32.765624 0-45.246093l-15.082031-15.082031c-12.503906-12.503907-32.769531-12.503907-45.25 0l-113.128906 113.128906-113.132813-113.152344c-12.5-12.5-32.765624-12.5-45.246093 0l-15.105469 15.082031c-12.5 12.503907-12.5 32.769531 0 45.25l113.152344 113.152344-113.128906 113.128906c-12.503907 12.503907-12.503907 32.769531 0 45.25l15.082031 15.082031c12.5 12.5 32.765625 12.5 45.246093 0l113.132813-113.132812 113.128906 113.132812c12.503907 12.5 32.769531 12.5 45.25 0l15.082031-15.082031c12.5-12.503906 12.5-32.769531 0-45.25zm0 0"
          />
        </svg>
      </div>
      <button :disabled="!text || !title" class="add-form__footer-button">Отправить</button>
    </div>
  </div>
</template>


<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  data() {
    return {
      title: "",
      text: ""
    };
  },
  methods: {
    clear() {
      this.title = "";
      this.text = "";
      console.log(this.$refs);
    }
  }
});
</script>