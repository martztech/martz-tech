<template>
  <section id="menu">
    <nav>
      <dl>
        <dt>
          <nuxt-link to="/ui-ux-design">User Interface &amp; User Experience Design</nuxt-link>
        </dt>
        <dd>
          <nuxt-link to="/front-end-developers">Front-End Development Services</nuxt-link>
        </dd>
        <dd>
          <nuxt-link to="/theme-design">HTML/CSS Template &amp; Theme Design</nuxt-link>
        </dd>
        <dd>
          <nuxt-link to="/javascript-animation">Animation &amp; Motion Design</nuxt-link>
        </dd>
        <dd>
          <nuxt-link to="/brand-design">Packacking &amp; Branding</nuxt-link>
        </dd>
      </dl>
    </nav>
    <nav>
      <dl>
        <dt>
          <nuxt-link to="/">Mechanical Prototype &amp; Product Design</nuxt-link>
        </dt>
        <dd>
          <nuxt-link to="/">CAD &amp; 3D Fabrication</nuxt-link>
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
    <nav>
      <dl>
        <dt>
          <nuxt-link to="/">Natural &amp; Regenerative Systems Design</nuxt-link>
        </dt>
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
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#menu {
  background: white;
  border-left: 1px solid black;
  height: 100vh;
  width: 360px;
  position: fixed;
  left: -360px;
  top: 0;
  bottom: 0;
  display: flex;
  flex-direction: column;
  nav {
    display: inline-block;
    margin: 0;
    padding: 0;
    width: 100%;
    dl {
      display: flex;
      flex-direction: column;
      margin: 0;
      padding: 0;
      dt {
        font-weight: 700;
      }
      dt,
      dd {
        display: inline-block;
        margin: 0;
        padding: 0;
        a {
          display: flex;
          width: 100%;
          padding: 5px 15px;
        }
        :hover {
          background: lightcyan;
        }
      }
    }
  }
}
</style>