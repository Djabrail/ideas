<template>
  <div class="container">
    <h3 class="main-title">Хочешь предложить тему?</h3>
    <AddForm />
    <Tabs />

    <div class="ideas">
      <!---->
      <IdeaItem />
    </div>
  </div>
</template>

<script>
import AddForm from "@/components/AddForm.vue";
import Tabs from "@/components/Tabs.vue";
import IdeaItem from "@/components/IdeaItem.vue";
export default {
  name: "Home",
  components: { AddForm, Tabs, IdeaItem }
};
</script>

<style lang="scss">
.main-title {
  font-weight: 600;
  font-size: 26px;
  line-height: 32px;
}

.add-form {
  margin: 30px 0;
  background: #fff;
  border: 1px solid #e5e7e9;
  box-sizing: border-box;
  box-shadow: 0 5px 10px rgba(0, 0, 0, 0.02);
  border-radius: 10px;
  padding: 25px 30px;
  cursor: text;

  input,
  textarea {
    width: 100%;

    &::-moz-placeholder {
      color: #cfcdcd; /* Цвет подсказывающего текста */
    }
    &::-webkit-input-placeholder {
      color: #cfcdcd;
    }
    &:-ms-input-placeholder {
      color: #cfcdcd;
    }
    &::-ms-input-placeholder {
      color: #cfcdcd;
    }
    &::placeholder {
      color: #cfcdcd;
    }
  }

  input {
    font-style: normal;
    font-weight: 700;
    font-size: 28px;
    margin-bottom: 15px;
  }
  textarea {
    font-size: 18px;
    resize: none;
  }

  &__footer {
    display: flex;
    align-items: center;
    justify-content: flex-end;

    button {
      background: #2c74ff;
      box-shadow: 0 5px 10px rgba(44, 116, 255, 0.2);
      border-radius: 6px;
      color: #fff;
      padding: 0 25px;
      height: 45px;
      font-size: 16px;
      font-weight: 600;
      letter-spacing: 0.5px;
      cursor: pointer;
      margin-right: 20px;
      transition: all 0.1s ease-in-out;

      &:hover {
        background-color: lighten(#2c74ff, 2%);
      }
      &:active {
        background-color: darken(#2c74ff, 3%);
      }

      &:disabled {
        background-color: #d1d7e2;
        cursor: not-allowed;
      }
    }

    svg {
      margin-right: 20px;
      cursor: pointer;

      path {
        fill: #d3d4d6;
      }

      &:hover {
        path {
          fill: #2c2c2c;
        }
      }
    }
  }
}

.tabs {
  display: flex;
  margin-bottom: 30px;

  a {
    text-decoration: none;
    color: inherit;
  }

  li {
    padding: 15px 25px;
    border-radius: 6px;
    font-weight: 600;
    cursor: pointer;
    margin-right: 10px;

    &:hover {
      background-color: lighten(#e7ebef, 3%);
    }

    &.active {
      color: #2c2c2c;
      background-color: #e7ebef;
    }
  }
}

.ideas {
  &__item {
    display: flex;
    align-items: center;
    background: #fff;
    border: 3px solid #e5e7e9;
    box-sizing: border-box;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.02);
    border-radius: 10px;
    padding: 25px 30px;
    position: relative;
    margin-bottom: 20px;

    &-details {
      flex: 1;
    }
    &-rating {
      margin-left: 20px;

      &-circle {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 64px;
        height: 64px;
        background: #f7f7f7;
        border-radius: 46px;
        cursor: pointer;

        &:hover {
          background-color: darken(#f7f7f7, 5%);
        }

        svg {
          position: relative;
          top: -2px;
        }
      }
      &-count {
        margin-top: 8px;
        text-align: center;
        font-weight: 700;
        font-size: 22px;
        color: #94989c;
      }
    }

    h3 {
      font-weight: 700;
      font-size: 28px;
      line-height: 34px;
      margin-bottom: 10px;
    }
    p {
      font-size: 18px;
      line-height: 26px;
    }
    &-footer {
      display: flex;
      margin-top: 15px;

      li {
        margin-right: 20px;
        svg {
          margin-right: 3px;
        }
      }
    }
  }
}
</style>