<template>
  <button class="c-button" :class="{ 'c-button--primary': type === 'primary' }">
    <div class="c-button-content">
      <Icon v-if="icon" name="{icon}" className="c-icon"></Icon>
      <slot />
    </div>
  </button>
</template>

<script lang="ts">
export default {
  props: {
    class: String,
    type: String,
    icon: String,
  },
};
</script>

<style lang="scss" scoped>
.c-link-route {
  width: 100%;
}

.c-button {
  min-height: 40px;
  left: 331px;
  border-radius: 28px;
  border: none;
  font-weight: 400;
  font-size: 14px;
  line-height: 17px;
  color: var(--color-black);
  width: 100%;
  font-family: "Arvo", serif;

  &-content {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  &:hover {
    cursor: pointer;
  }

  &:active {
    transform: scale(0.98);
    box-shadow: 3px 2px 22px 1px rgba(0, 0, 0, 0.24);
  }

  .c-icon {
    margin: 0 20px 0 20px;
    width: 20px;
    height: 20px;
  }

  &--primary {
    color: var(--color-white);
    background-color: var(--color-primary);
  }
}
</style>
