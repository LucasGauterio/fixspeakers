<template>
    <v-footer color="primary">
        <v-row justify="center" no-gutters>
            <v-btn v-for="link in links" :key="link" color="white" variant="text" class="mx-2" rounded="xl">
                <a :href="link.url" target="_blank">
                    {{ link.title }}
                </a>
            </v-btn>
            <v-col class="text-center mt-4" cols="12">
                2023 — <strong>{{ $t('title') }}</strong>
            </v-col>
        </v-row>
    </v-footer>
</template>
<style scoped>
a {
  text-decoration: none;
  color: white;
}
</style>
<script>
  export default {
    data: () => ({
      links: [
        {title: 'Privacy Policy', url: `${window.location.href}/privacypolicy.html`},
      ],
    }),
  }
</script>