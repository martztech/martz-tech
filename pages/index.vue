<template>
  <div class="page-index">
    <div class="container">
      <nuxt-link to="/blogs/bacon-ipsum">bacon</nuxt-link>
    </div>
  </div>
</template>

<script>
import blogsEn from "~/contents/en/blogsEn.js";
import blogsEs from "~/contents/es/blogsEs.js";

export default {
  transition: {
    name: "slide-fade"
  },

  head() {
    return {
      title: "Martz Technologies | Radical thinking in design",
      htmlAttrs: {
        lang: this.$i18n.locale
      },
      script: [
        { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" }
      ],
      meta: [
        { name: "author", content: "Troy Martz" },
        {
          name: "description",
          property: "og:description",
          content: this.$t("indexPageHead.description"),
          hid: "description"
        },
        { property: "og:title", content: this.$t("indexPageHead.title") },
        { property: "og:image", content: this.ogImage },
        {
          name: "twitter:description",
          content: this.$t("indexPageHead.description")
        },
        { name: "twitter:image", content: this.ogImage }
      ]
    };
  },

  computed: {
    ogImage: function() {
      return;
    }
  }
};
</script>
