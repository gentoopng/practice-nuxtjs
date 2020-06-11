<template>
    <section class="hero is-info is-bold">
        <div class="hero-body">
            <h1 class="title is-size-2">
                Contact
            </h1>
            <h2 class="subtitle is-size-4">
                お問い合わせ
            </h2>
        </div>
    </section>
</template>

<script>
export default {
  fetch ({store}) {
    store.commit('resetMenu')
  }
}
</script>