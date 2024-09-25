<template>
  <div>

    <windowjs-style-metal>
      <template v-for="i in [1, 2, 3, 4]" , :zGroup="0">
        <windowjs :key="i" :title="`Base Layer #${i}`">
          <fieldset>
            <legend>&alpha;</legend>
            <input type="range" />
          </fieldset>
        </windowjs>
      </template>
    </windowjs-style-metal>

    <windowjs-style-black>
      <template v-for="i in [1, 2, 3, 4]">
        <windowjs :key="i" :title="`Floating Layer #${i}`" :zGroup="1">
          <fieldset>
            <legend>&alpha;</legend>
            <input type="range" />
          </fieldset>
        </windowjs>
      </template>
    </windowjs-style-black>

    <p>
      Floating windows always appear in foreground of windows on base layer.
    </p>
  </div>
</template>