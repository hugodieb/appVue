<template>
  <header class="phone-viewport">
    <md-toolbar>
      <md-button class="md-icon-button" v-on:click.native="toggleLeftSideBar">
        <md-icon>menu</md-icon>
      </md-button>

      <h1 class="md-title">{{ title }}</h1>
    </md-toolbar>

      <md-sidenav class="md-left" ref="leftSidenav">
        <md-toolbar class="md-medium">
          <div class="md-toolbar-container">
            <h2 class="md-title">Sidenav Content</h2>
          </div>
        </md-toolbar>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit.
          Nam libero eros, lobortis at neque venenatis, tincidunt sollicitudin nibh.
          Etiam et risus arcu. Sed ornare neque vitae placerat dictum.
        </p>
      </md-sidenav>

  </header>
</template>

<script>

export default {
  name: 'SchoolWeb',

  data () {
    return {
      title: 'Ecommerce SchoolWeb'
    }
  },

  methods: {
    toggleLeftSideBar () {
      this.$refs.leftSidenav.toggle()
    }
  }
}
</script>

<style>
</style>
