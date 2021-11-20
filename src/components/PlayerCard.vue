<template>
    <div>
        <div class="card mb-3" style="max-width: 540px;">
            <div class="row g-0">
                <div class="col-md-4">
                    <img :src="player.avatar_url" class="img-fluid rounded-start" alt="player avatar">
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <h5 class="card-title">{{player.name}}</h5>
                        <p class="card-text" v-if="player.bio">{{player.bio}}</p>
                        <p class="card-text" v-else>This is a wider card with supporting text below as a natural lead-in
                            to additional content. This content is a little bit longer.</p>
                        <p class="card-text"><small class="text-muted">Joind: {{player.created_at}}</small></p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    //import axios from 'axios'

    export default ({
        name: 'player-card',
        props: ['player']
        // data () {
        //     return {
        //         user: {

        //         }
        //     }
        // },
        // created () {
        //     axios.get(`https://api.github.com/users/${this.username}`)
        //     .then(response => {
        //         this.user = response.data
        //     })
        // }
    })
</script>