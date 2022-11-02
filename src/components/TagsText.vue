<template>
  <div class="tags-text" :class="styleObject">
    <div class="tags-text__title">{{ title }}</div>
    <div class="tags-text__wrapper">
      <div
        class="tags-text__item"
        v-for="(item, index) in text"
        :key="item.text"
      >
        <v-icon>
          {{ `mdi-${item.icon}` }}
        </v-icon>
        <div class="tags-text__content">{{ item.text }}</div>
        <v-icon class="tags-text__icon" size="7" v-if="index <= text.length - 2"
          >mdi-circle</v-icon
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TagsText',
  props: {
    align: {
      type: String,
      default: 'center',
    },
    text: {
      type: Array,
      default: () => {
        return [{}];
      },
    },
    title: {
      type: String,
      default: '',
    },
  },
  computed: {
    styleObject() {
      return {
        'tags-text--left': this.align === 'left',
      };
    },
  },
};
</script>

<style lang="scss" scoped>
.tags-text {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  &--left {
    align-items: flex-start;
  }
  &__item {
    display: flex;
  }
  &__wrapper {
    display: flex;
    flex-wrap: wrap;
    height: 1.5em;
    overflow: hidden;
  }
  &__content {
    display: flex;
    margin-right: 10px;
    white-space: nowrap;
  }
  &__icon {
    display: flex;
    margin-right: 10px;
  }
  &__title {
    display: inline;
  }
}
</style>
