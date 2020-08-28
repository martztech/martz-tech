<template>
  <div class="layout">
    <header>
      <section>
        <div>
          <div>
            <h1>Martz Technologies</h1>
            <h3>Radical Thinking In Systems Design</h3>
          </div>
        </div>
      </section>

      <nav>
        <dl>
          <dt>Software &amp; Application &amp; Website Design</dt>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
        </dl>
        <dl>
          <dt>Mechanical Prototype &amp; Product Design</dt>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
        </dl>
        <dl>
          <dt>Natural &amp; Regenerative Systems Design</dt>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/">ABC</nuxt-link>
          </dd>
        </dl>
      </nav>
    </header>
    <nuxt class="nuxt-content"/>
    <Footer/>
  </div>
</template>
<script>
import Footer from "~/components/Sections/Footer";

export default {
  components: {
    Footer
  }
};
</script>
<style lang="scss">
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.nuxt-content {
  flex-grow: 1;
}
</style>
