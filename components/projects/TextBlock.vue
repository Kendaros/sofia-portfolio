<template>
  <div class="text-block">
    <h3 class="subtitle">
      {{ subtitle }}
    </h3>
    <h2 class="title">
      {{ title }}
    </h2>
    <div
      class="text"
      v-html="text"
    />
  </div>
</template>

<script>
export default {
  name: 'TextBlock',

  props: {
    subtitle: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    },
    text: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss">
@import "~@/assets/style/variables";

.text-block {
  .subtitle {
    font-size: $f20;
    line-height: $f26;
    text-transform: uppercase;
    font-weight: normal;

    @media screen and (max-width: $breakpoint-sm) {
      font-size: $f18;
    }
  }

  .title {
    font-family: $zilla_slab;
    font-size: $f56;
    line-height: $f48;
    margin: 24px 0;

    @media screen and (max-width: $breakpoint-sm) {
      font-size: $f40;
      line-height: $f32;
    }
  }

  .text {
    font-size: $f18;
    line-height: $f28;

    @media screen and (max-width: $breakpoint-sm) {
      font-size: $f16;
      line-height: $f27;
    }

    & > p {
      text-indent: 30px;
    }
  }
}

</style>
