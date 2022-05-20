<template>
  <div>
    <label class="p-3 text-center" for="filter-search"
        >Filtra per artista
        <select @change="$emit('searchAuthorSelected', searchAuthor)" v-model="searchAuthor" class="my-1" name="filter-author" id="filter-author">
        <option value="" selected>Tutti</option>
        <option value="Bon Jovi">Bon Jovi</option>
        <option value="Queen">Queen</option>
        <option value="Sting">Sting</option>
        <option value="Steve Gadd Band">Steve Gadd Band</option>
        <option value="Iron Maiden">Iron Maiden</option>
        <option value="Eric Clapton">Eric Clapton </option>
        <option value="Deep Purple">Deep Purple</option>
        <option value="Metallica">Metallica</option>
        <option value="Dave Weckl">Dave Weckl</option>
        <option value="Michael Jacjson">Michael Jacjson</option>
        </select>
    </label>
  </div>
</template>

<script>
export default {
    name: "AppAuthorSearch",
    data() {
    return {
      searchAuthor: "",
    };
  },
};
</script>

<style scoped lang="scss">

label {

  color: white;

  select {
    min-width: 6rem;
  }
}

option, select, label {
    font-weight: 600;
}

</style>