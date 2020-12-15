<template>
  <b-table :data="livres" :columns="columns" default-sort="titre" defaults-sort-direction="asc"></b-table>
</template>

<script>
import axios from "axios";

export default {
  name: 'App',
  data() {
    return {
      livres: [],
      columns: [
        {
            field: 'titre',
            label: 'Titre de l\' oeuvre',
            searchable: true,
            sortable: true
        },
        {
            field: 'auteur',
            label: 'Auteur de l\'oeuvre',
            searchable: true,
            sortable: true
        },
        {
            field: 'maisonEdition',
            label: 'Maison d\'édition de l\'oeuvre',
            numeric: true,
            sortable: true
        },
        {
            field: 'edition',
            label: 'Édition de l\'oeuvre',
            numeric: true,
            sortable: true
        }
      ]
    }
  },
  created: function() {
    this.getLivres()
    setInterval(this.getLivres,3000)
  },
  methods: {
    getLivres(){
      axios
        .get("http://localhost:3000/livre")
        .then(res => {
          this.livres = res.data
        })
    }
  }
    
}
</script>
