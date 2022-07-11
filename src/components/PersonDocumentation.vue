<template>
  <section class="text-start text-black">
    <h1 class="fw-bolder ps-4">Документација со барање за лизинг: ПРАВНИ ЛИЦА</h1>
    <p class="fs-4">Со пополнето барање за одобрување на лизинг, профактура на
      добавувачот и прифатена лизинг понуда, потребно е да се приложат и:
    </p>
    <ul v-for="documentation in PersonDocumentation" class="ps-5">
      <li>
        <h3>{{ documentation.description }}
          <a v-if="documentation.linkName !== ''" :href=documentation.goToLink class="fw-bold fs-4">({{ documentation.linkName }})</a>
        </h3>
      </li>
    </ul>
    <p class="fw-bold fs-4">Документација треба да биде заверена со потпис и печат на овластеното лице!</p>
    <p class="fs-4 mb-4"><strong>AUTOWELT</strong> го задржува правото да побара дополнителна документација за разгледување на барањата за одобрување на лизинг.</p>
    <hr class="mb-5">
  </section>

</template>

<script>
export default {
  name: "LawPerson",
  props: {
   PersonDocumentation: Array,
  }
}
</script>

<style scoped>

</style>