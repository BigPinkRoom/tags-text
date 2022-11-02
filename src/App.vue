<template>
  <v-app>
    <v-main>
      <div class="tags-text__wrapper">
        <TagsText
          align="center"
          :text="textContent"
          title="Текстовый заголовок"
        />
      </div>
    </v-main>
  </v-app>
</template>

<script>
import TagsText from '@/components/TagsText';

export default {
  name: 'App',

  components: {
    TagsText,
  },
  data() {
    return {
      textContent: [
        {
          text: '5',
          icon: 'star',
        },
        {
          text: 'Обзорная',
          icon: '',
        },
        {
          text: 'На автобусе',
          icon: 'bus',
        },
        {
          text: '25 марта',
          icon: '',
        },
        {
          text: '6 часов',
          icon: 'clock',
        },
      ],
      textTitle: {},
    };
  },
};
</script>
<style lang="scss" scoped>
.tags-text {
  &__wrapper {
    background-color: #f0f0f0;
    margin: 100px;
    padding: 10px;
    border-radius: 5px;
    border: 1px solid #ccc;
  }
}
</style>
