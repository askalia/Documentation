<template>
  <div class="logo" @contextmenu="rightClick" oncontextmenu="return false;">
    <g-link class="logo__link" to="/" title="Back to home">
      <LogoDark class="logo__svg hide-for-small" alt="Gridsome.org" />

      <LogoSmall
        class="logo__svg show-for-small logo__svg--small"
        alt="Gridsome.org"
      />
    </g-link>
  </div>
</template>

<script>
import LogoDark from "~/assets/images/8base-logo-white.svg";
import LogoSmall from "~/assets/images/8base-logo.svg";
export default {
  props: ["theme"],
  components: {
    LogoDark,
    LogoSmall
  },
  methods: {
    rightClick() {
      this.$router.push({ path: "/logo" });
      return false;
    }
  }
};
</script>

<style lang="scss">
.logo {
  &__svg {
    max-width: 130px;
    height: auto;
    margin-top: -3px;
    &--small {
      max-width: 25px;
    }
  }
}
</style>
