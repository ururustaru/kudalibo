<template>
	<button>
		<slot name="icon"></slot>
		<slot name="text"></slot>
	</button>
</template>

<script>
	export default {
	}
</script>

<style lang="scss">
  @import '~assets/scss/variables';

  .btn {
    display: inline-flex;
    padding: 13px 25px;
    background: $accent-color;
    color: $light;
    justify-content: center;
    align-items: center;
    border: none;
    box-shadow: $accent-btn-shadow;
    border-radius: 6px;
    font-size: 18px;
    font-weight: 400;
    cursor: pointer;
    outline: none;
  
    svg {
      margin-right: 8px;
    }
  
    &:hover {
      box-shadow: none;
    }
  
    &:disabled {
      box-shadow: $pressed-btn-shadow;
      background: $text-gray-dark;
    }
  
    &--dark {
      background: $main-text-color;
      box-shadow: $dark-btn-shadow;
      padding: 12px 25px;
      height: 50px;
      white-space: nowrap;
    }
  
    &--white {
      background: $light;
      color: $accent-color;
    }
  
    &--alt {
      background: $accent-alt-color;
      box-shadow: none;
    }
  
    &--no-text {
      font-size: 0;
    
      svg {
        margin-right: 0;
      }
    
      &.btn--dark {
        width: 56px;
        height: 56px;
        padding: 0;
      }
    }
  
    &--rounded {
      border-radius: 28px;
    }
  
    &--gray {
      background: $main-text-light;
      color: $light;
      border: 1px solid $main-text-light;
      box-shadow: none;
    
      &:hover {
        background: $text-gray-dark;
        border-color: $text-gray-dark;
      }
    }
  }
</style>
