<template>
    <div>
        <div class="row">
            <div class="col" v-for="(user, index) in users" :key="index">
                <div>
                    <div class="card m-3">
                        <img :src="user.avatar_url" class="card-img-top" alt="">
                        <div class="card-body">
                            <h5 class="card-title">{{user.name}}</h5>
                            <p class="card-text">{{user.bio}}</p>
                            <p class="text-muted"><a :href="user.html_url" target="_blank">Repos: {{ parseInt(user.public_repos) }} </a></p>
                            <p class="text-muted">Followers: {{ parseInt(user.followers) }} </p>
                            <button class="btn btn-primary" 
                            @click="$emit('openCard', user)">View Details</button>
                    
                        </div>
                    </div>
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