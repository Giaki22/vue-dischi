<template>
  <div class="selection">
            <label for="filter">FILTRA PER TIPO</label>
            <select id="filter" v-model="data.filterValue">
                <option disabled value="">Select Genre</option>
                <option>Pop</option>
                <option>Jazz</option>
                <option>Metal</option>
                <option>Rock</option>
            </select>
        </div>
</template>

<script>
import data from '../../shared/data.js'

export default {
    name:'AselectionFilter',
    data() {
        return {
            data
        }
    }
}
</script>

<style>
label{
    margin-right: .625rem;
}
</style>