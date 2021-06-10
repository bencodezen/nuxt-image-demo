<template>
  <div class="container">
    <div>
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
export default {};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
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
