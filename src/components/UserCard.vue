<template>
    <div>
        <div class="card" style="width: 18rem;">
            <img :src="user.avatar_url" class="card-img-top" alt="">
            <div class="card-body">
                <h5 class="card-title">{{user.name}}</h5>
                <p class="card-text">{{user.bio}}</p>
                <a :href="user.html_url" class="btn btn-primary" target="_blank">Go to GitHub</a>
            </div>
        </div>
    </div>
</template>

<script>

//import axios from 'axios'

export default ({
    name: 'user-card',
    props: ['user']
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
