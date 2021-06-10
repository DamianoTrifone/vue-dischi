<template>
    <select name="genre" id="genre" v-model="selected" @change="$emit('selectGender', selected)">
        <option disabled>Seleziona il genere</option>
        <option value="all">Tutti</option>
        <option value="pop">Pop</option>
        <option value="rock">Rock</option>
        <option value="jazz">Jazz</option>
        <option value="metal">Metal</option>
    </select>
</template>

<script>
export default {
    data() {
        return {
            selected: ''
        }
    }
}
</script>

<style>
    select{
        float: right;
    }
</style>
