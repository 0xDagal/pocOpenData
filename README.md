# Interface

/!\ N'utilisez pas ce code en production il n'est pas sécurisé et est là
uniquement à but de démonstration.

## Description

L'interface est faites en VueJS grâce à vue-cli avec comme UI Component Buefy
et Axios pour la récupération des données.

## Tableau

Le tableau est un simple tableau tel que l'on peut retrouver dans la
documentation de Buefy (Buefy est une UI Component pour VueJS se basant sur le
framework CSS/SCSS Bulma).

## Récupération des données

Au moment de la création du composant App.Vue (qui est le composant de base de
VueJS), on fait un appel en GET grâce à Axios puis on appelle la méthode
getLivres qui va faire cette appel et on rappelle cette méthode toutes les 3s.
