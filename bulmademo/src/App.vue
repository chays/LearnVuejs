<template>
  <div id="app">
    <div class="container">
      <div class="notification">
        This container is <strong>centered</strong> on desktop.
      </div>
    </div>
    <!-- 2 -->
    <div class="container is-fluid">
      <div class="notification">
        This container is <strong>centered</strong> on desktop.
      </div>
    </div>
    <!-- 3 -->
    <div class="container is-widescreen">
      <div class="notification">
        This container is <strong>fullwidth</strong> <em>until</em> the <code>$widescreen</code> breakpoint.
      </div>
    </div>
    <!-- 4 -->
    <div class="container is-fullhd">
      <div class="notification">
        This container is <strong>fullwidth</strong> <em>until</em> the <code>$fullhd</code> breakpoint.
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'app',
}
</script>
