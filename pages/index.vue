<template>
  <div class="container">
    <h1>Nuxt Image Demo</h1>
    <h2>Image Selection</h2>
    <nuxt-img :src="selectedImage" sizes="xl:75vw lg:50vw" alt="" />
    <div>
      <select name="select-images" id="select-images" v-model="selectedImage">
        <option value="">Default</option>
        <option
          v-for="image in imageList"
          :key="image.label"
          :value="image.url"
          >{{ image.label }}</option
        >
      </select>
      <nuxt-img src="/unsplash.jpg" sizes="xl:100vw lg:75vw" alt="" />
      <p>
        Photo by
        <a
          href="https://unsplash.com/@rev3n?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText"
        >
          Michał Kubalczyk
        </a>
        on
        <a
          href="https://unsplash.com/t/technology?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText"
        >
          Unsplash</a
        >
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    imageList: [
      {
        label: "Ocean",
        url:
          "https://images.unsplash.com/photo-1601649705707-13b54dc57b87?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1426&q=80"
      },
      {
        label: "Mountain Top",
        url:
          "https://images.unsplash.com/photo-1604051189201-700f955d1cf8?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1500&q=80"
      },
      {
        label: "Comet",
        url:
          "https://images.unsplash.com/photo-1623284577359-a0130bb9a86d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1500&q=80"
      }
    ],
    selectedImage: ""
  })
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
