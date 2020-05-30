<template>
  <div id="app">
    <Menus
      refresh
      debug
      :flyout="[
      {
        label: 'This flyout menu has a JSON structure'
      }]"
    />
    <Panel>
      <Wrapper>
        <Anno size="42px">Has hot reloading</Anno>
        <Input-Scroll label="Numeric value" :value="10" @update="val => number = val" />
        <Button label="Click me" :evalScript="`sendMsg('Hello ${number}')`" />
      </Wrapper>
    </Panel>
  </div>
</template>

<script>
export default {
  data: () => ({
    number: 10
  })
};
</script>
