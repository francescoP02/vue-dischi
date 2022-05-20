<template>
  <div>
    <label class="p-3 text-center" for="filter-search"
        >Filtra per genere musicale
        <select @change="$emit('searchSelected', searchText)" v-model="searchText" class="my-1" name="filter-search" id="filter-search">
        <option value="" selected>Tutti</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
        </select>
    </label>
  </div>
</template>

<script>
export default {
    name: "AppSearch",
    data() {
    return {
      searchText: "",
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