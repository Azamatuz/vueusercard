<template>
    <div>
        <div class="row">
            <div class="col" v-for="(player, index) in players" :key="index">
                <div>
                    <div class="card m-3">
                        <img :src="player.avatar_url" class="card-img-top" alt="">
                        <div class="card-body">
                            <h5 class="card-title">{{player.name}}</h5>
                            <p class="card-text">{{player.bio}}</p>
                            <p class="text-muted"><a :href="player.html_url" target="_blank">Repos: {{ parseInt(player.public_repos) }} </a></p>
                            <p class="text-muted">Followers: {{ parseInt(player.followers) }} </p>
                            <button class="btn btn-primary" 
                            @click="$emit('openCard', player)">View Details</button>
                    
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'player-list',
        props: ['players', 'player']
    }
</script>