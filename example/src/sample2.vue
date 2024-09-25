<template>
  <windowjs-style-metal>

    <windowjs title="Window 1" :resizable="true" :isMiniSize.sync="isMiniSize"
    :miniButton="true" :closeButton="true" :isOpen.sync="isOpen">
      Parameters:
      <fieldset>
        <legend>&alpha;</legend>
        <input type="range" />
      </fieldset>
      <fieldset>
        <legend>&beta;</legend>
        <input type="range" />
      </fieldset>
    </windowjs>

    <button @click="isOpen = ! isOpen">Toggle Window 1</button>

  </windowjs-style-metal>
</template>


<script lang="ts">
export default <any>{
  data() {
    return {
      isOpen: true,
      isMiniSize: false,
    }
  },
}
</script>