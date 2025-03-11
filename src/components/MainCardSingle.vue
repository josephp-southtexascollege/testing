<script setup>
    import { faker } from '@faker-js/faker'
    const firstName = faker.person.firstName()
    const lastName = faker.person.lastName()
    
</script>

<template>
    {{ firstName }} {{ lastName }} <br/>

</template>