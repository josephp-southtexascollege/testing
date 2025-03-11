<script setup>
    import { faker } from '@faker-js/faker'
    const firstname = faker.person.firstName()
    const lastname = faker.person.lastName()
    const jobtitle = faker.person.jobTitle()
    const bio = faker.lorem.lines(2)
const username = faker.internet.username({ firstName: firstname, lastName: lastname }).toLowerCase()
</script>

<template>
    <RouterLink :to="{name: 'CardDetail', params:{id: username}}">
        <div class="border broder-gray-500 rounded-lg shawdow bg-gray-400">
            <img class="object-fill h-64 w-96 rounded-lg" v-bind:src="faker.image.avatar()"/> 
            <div class="p-4">
                <p class="mb-2 text-2xl font-bold">{{ firstname }} {{ lastname }}</p>
                <p class="mb-3 font-normal text-gray-800">{{ jobtitle }}</p>
                <p class="mb-3 font-normal text-gray-800">{{ bio }}</p>
            </div>
        </div>
    </RouterLink>
</template>