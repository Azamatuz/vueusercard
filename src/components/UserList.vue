<template>
    <div>
        <div class="row">
            
        </div>
        <div v-for="(user, index) in users" :key="index">
            <div class="card" style="width: 18rem;">
                <img :src="user.avatar_url" class="card-img-top" alt="">
                <div class="card-body">
                    <h5 class="card-title">{{user.name}}</h5>
                    <p class="card-text">{{user.bio}}</p>
                    <a :href="user.html_url" class="btn btn-primary" target="_blank">Go to GitHub</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'user-list',
        props: ['users', 'user']
    }
</script>