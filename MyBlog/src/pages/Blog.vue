<template>
  <Layout>
    <section>
      <h1>Blog</h1>
      <ul>
      <li v-for="{ node } in $page.posts.edges" :key="node.id">
        <g-link :to="node.path">
       <div>
        <h1 class="">  {{node.title}}  </h1>
        <strong >{{url}}</strong> 
        <p id="description"> {{node.description}}</p>
        <p class=""> Posted on {{node.date}} </p>
        </div>
        </g-link>
      </li>
    </ul>
    </section>
  </Layout>
</template>
<page-query>
query Posts {
    posts: allContentfulBlogPost {
    edges {
      node {
        id,
        title,
        description,
        date (format: "MMMM DD, YYYY"),
        path
        heroImage{
          file{
            url
          }
        }
      }
    }
      }
    }
</page-query>
<script>
  export default {
    metaInfo: {
    title: 'blog'
    },
    data(){
    return{
      
    }
    },
    methods:{
      converImage(image){
        this.url = image.file.url
      }
    }
  };
</script>

