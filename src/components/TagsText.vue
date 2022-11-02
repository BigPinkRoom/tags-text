<template>
  <div class="tags-text">
    <div class="tags-text__title">{{ title }}</div>
    <div class="tags-text__wrapper">
      <div class="tags-text__item" v-for="item in text" :key="item.text">
        <v-icon>
          {{ `mdi-${item.icon}` }}
        </v-icon>
        <div class="tags-text__content">{{ item.text }}</div>
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
};
</script>

<style lang="scss" scoped>
.tags-text {
  &__item {
    display: flex;
  }
  &__wrapper {
    display: flex;
  }
}
</style>
