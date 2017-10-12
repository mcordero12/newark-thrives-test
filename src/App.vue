<template>
  <div id="app">
    <Slideout menu="#menu" panel="#panel" :toggleSelectors="['.toggle-button']" @on-open="open">
      <nav id="menu">
        <div><h3>Program Categories</h3></div>
        <nt-sidebaritems></nt-sidebaritems>
      </nav>
      <main id="panel">
        <header>
          <div id="combined-header">
            <button class="toggle-button">☰</button>
            <nt-header></nt-header>
          </div>
        </header>
        <nt-mapview></nt-mapview>
      </main>
    </Slideout>
  </div>
</template>

<script>
  import Header from './components/Header.vue';
  import MapView from './components/MapView.vue';
  import SidebarItems from './components/SidebarItems.vue';
  import Slideout from 'vue-slideout'

  export default {
    components: {
      'nt-header': Header,
      'nt-mapview': MapView,
      'nt-sidebaritems': SidebarItems,
      Slideout
    }
  }
</script>

<style>
  html, body {
    height: 100%;
    margin: 0px;
    padding: 0px;
  }

  .slideout-menu {
    position: fixed;
    top: 0;
    bottom: 0;
    width: 256px;
    height: 100vh;
    overflow-y: scroll;
    -webkit-overflow-scrolling: touch;
    z-index: 0;
    display: none;
    background-color: #ffd700;
    color:navy;
  }

  .slideout-menu-left {
    left: 0;
  }

  .slideout-menu-right {
    right: 0;
  }

  .slideout-panel {
    background-color: #fff;
    color: white;
    position: relative;
    z-index: 1;
    will-change: transform;
    min-height: 100vh;
  }

  .slideout-open,
  .slideout-open body,
  .slideout-open .slideout-panel {
    overflow: hidden;
  }

  .slideout-open .slideout-menu {
    display: block;
  }

  .toggle-button {
    background-color: navy;
    color: #ffd700;
    border: none;
    padding: 5px 10px;
    font-size: 18px;
  }

  #combined-header {
    display: flex;
    position: static;
  }
</style>
