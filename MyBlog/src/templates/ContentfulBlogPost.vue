<template>
  <Layout>
    <div class="markdown">
    <h1>{{$page.post.title}}</h1>
    <p> Posted on {{$page.post.date}} </p>
    <div id="body" v-html="$page.post.body"></div>

    <div>
     <vue-disqus shortname="https-connorreilly-netlify-app" :identifier="$page.post.id"></vue-disqus>
    </div>
    </div>
  </Layout>
</template>

<page-query>
query Post ($path: String!) {
  post: contentfulBlogPost (path: $path) {
    title,
    body(html:true),
    date (format: "MMMM DD, YYYY"),
    path
  }
}
</page-query>

<script>
  import { documentToHtmlString } from '@contentful/rich-text-html-renderer'

  export default {
    methods: {
    richtextToHTML (content) {
      return documentToHtmlString(content)
    }
  }
}
 
</script>
<style>
#body{
  color: #2d3748;
}
#body h1 {
  font-size: 20px;
  padding-bottom: 10px;
  padding-top: 10px;
}
#body hr{
  padding-bottom: 10px;
}
#body pre{
  background-color: #2d3748;
  color: #a0aec0;
  margin: 20px;
  padding: 20px;
  border-radius: 20px;
  display: flex;
  flex-wrap: wrap;
  
}
#body pre code{ 
  overflow: scroll;
  max-height: 400px;
}
#body ul li{
  list-style-position: inside;
  list-style-type: square;
}
#body ol{
  padding-top: 10px;
  padding-bottom:  10px ;
  font-size: 20px;
  list-style-type: decimal;
  list-style-position: inside;
}
</style>