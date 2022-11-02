<template>
  <v-app>
    <v-main>
      <TagsText
        align="center"
        :text="textContent"
        title="Текстовый заголовок"
      />
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
