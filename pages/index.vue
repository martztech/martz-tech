<template>
  <div class="page-index">
    <div class="container">
      <nuxt-link to="/blog/design-thinking">Design Thinking</nuxt-link>

      <BlogSection :blogs="blogs"/>
    </div>
  </div>
</template>

<script>
import BlogSection from "~/components/Sections/BlogSection";

import blogsEn from "~/contents/en/blogsEn.js";
import blogsEs from "~/contents/es/blogsEs.js";

export default {
  async asyncData({ app }) {
    const blogs = app.i18n.locale === "en" ? blogsEn : blogsEs;

    async function asyncImport(blogName) {
      const wholeMD = await import(`~/contents/${
        app.i18n.locale
      }/blog/${blogName}.md`);
      return wholeMD.attributes;
    }

    return Promise.all(blogs.map(blog => asyncImport(blog))).then(res => {
      return {
        blogs: res
      };
    });
  },

  components: { BlogSection },

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
