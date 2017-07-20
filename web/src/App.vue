<template>
 <div class="phone-viewport">
  <md-toolbar>
    <md-button class="md-icon-button" @click="toggleLeftSidenav">
      <md-icon>menu</md-icon>
    </md-button>

    <h2 class="md-title">{{title}}</h2>

  </md-toolbar>

  <md-sidenav class="md-left" ref="leftSidenav" @open="open('Left')" @close="close('Left')">
    <md-toolbar class="md-large">
      <div class="md-toolbar-container">
        <h3 class="md-title">Navegação</h3>
      </div>
      <md-list>
        <md-list-item>
          Perfil
        </md-list-item>
        <md-list-item>
          <router-link to="/categories">Categoria</router-link>
        </md-list-item>
        <md-list-item>
          <router-link to="/products">Produtos</router-link>
        </md-list-item>
        <md-list-item>
          Sair
        </md-list-item>
      </md-list>
    </md-toolbar>
  </md-sidenav>
  <md-row>
    <router-view></router-view>
  </md-row>
</div>
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
    toggleLeftSidenav () {
      this.$refs.leftSidenav.toggle()
    }
  }
}
</script>

<style>
</style>
