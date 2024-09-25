<template>
  <windowjs-style-metal>

    <windowjs title="Center" positionHint="center">
      <fieldset>
        <legend>&alpha;</legend>
        <input type="range" />
      </fieldset>
    </windowjs>

    <windowjs title="Right Bottom" positionHint="-20 / -100">
      <fieldset>
        <legend>&alpha;</legend>
        <input type="range" />
      </fieldset>
    </windowjs>

    <windowjs title="Bottom Left" positionHint="20 / -200">
      <fieldset>
        <legend>&alpha;</legend>
        <input type="range" />
      </fieldset>
    </windowjs>

    <windowjs title="Top Right" positionHint="-20 / 20">
      <fieldset>
        <legend>&alpha;</legend>
        <input type="range" />
      </fieldset>
    </windowjs>

    <template v-for="i in [1, 2, 3, 4]">
      <windowjs :key="i" :title="`Auto-${i}`">
        <fieldset>
          <legend>&alpha;</legend>
          <input type="range" />
        </fieldset>
      </windowjs>
    </template>

    <windowjs title="Sync-A" :left.sync="x" :top.sync="y">
      <fieldset>
        <legend>&alpha;</legend>
        <input type="range" />
      </fieldset>
    </windowjs>

    <windowjs title="Sync-B" :left="x + 200" :top="y">
      <fieldset>
        <legend>&alpha;</legend>
        <input type="range" />
      </fieldset>
    </windowjs>

  </windowjs-style-metal>
</template>


<script>
export default {
  data() {
    return {
      x: null,
      y: null,
    }
  }
}
</script>
