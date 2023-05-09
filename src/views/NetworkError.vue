<template>
  <div class="networkError">
    <h1>Uh-Oh!</h1>

    <h3>It looks like you're experiencing some network issues.</h3>
    <h3>
      please take a breath and
      <a href="#" class="no-text-dec" @click="$router.go(-1)">click here</a> to
      try again.
    </h3>
  </div>
</template>
