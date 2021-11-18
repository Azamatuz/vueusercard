<template>
  <div id="App">
    <div class="container">
    <user-card :user="userCard"
    v-if="userCard" />
    <user-list 
    :users="users"
    :user="userCard"
    @openCard="openCard"/>
    </div>
  </div>
</template>

<script>
import UserCard from '@/components/UserCard'
import UserList from './components/UserList.vue'


export default {
  name: 'App',
  data() {
    return {
      userCard:'',
      users: [
        {
        login: "Azamatuz",
        id: 5535590,
        node_id: "MDQ6VXNlcjU1MzU1OTA=",
        avatar_url: "https://avatars.githubusercontent.com/u/5535590?v=4",
        gravatar_id: "",
        url: "https://api.github.com/users/Azamatuz",
        html_url: "https://github.com/Azamatuz",
        followers_url: "https://api.github.com/users/Azamatuz/followers",
        following_url: "https://api.github.com/users/Azamatuz/following{/other_user}",
        gists_url: "https://api.github.com/users/Azamatuz/gists{/gist_id}",
        starred_url: "https://api.github.com/users/Azamatuz/starred{/owner}{/repo}",
        subscriptions_url: "https://api.github.com/users/Azamatuz/subscriptions",
        organizations_url: "https://api.github.com/users/Azamatuz/orgs",
        repos_url: "https://api.github.com/users/Azamatuz/repos",
        events_url: "https://api.github.com/users/Azamatuz/events{/privacy}",
        received_events_url: "https://api.github.com/users/Azamatuz/received_events",
        type: "User",
        site_admin: false,
        name: "Azamat Uzbekov",
        company: "UoS",
        blog: "",
        location: "Saskatoon, SK, Canada",
        email: null,
        hireable: true,
        bio: "Friendly tv advocate. Infuriatingly humble entrepreneur. Travel nerd. Future teen idol.",
        twitter_username: null,
        public_repos: 39,
        public_gists: 0,
        followers: 1,
        following: 5,
        created_at: "2013-09-25T06:18:03Z",
        updated_at: "2021-08-08T03:28:56Z"
      },
      {
        login: "alan",
        id: 6356,
        node_id: "MDQ6VXNlcjYzNTY=",
        avatar_url: "https://avatars.githubusercontent.com/u/6356?v=4",
        gravatar_id: "",
        url: "https://api.github.com/users/alan",
        html_url: "https://github.com/alan",
        followers_url: "https://api.github.com/users/alan/followers",
        following_url: "https://api.github.com/users/alan/following{/other_user}",
        gists_url: "https://api.github.com/users/alan/gists{/gist_id}",
        starred_url: "https://api.github.com/users/alan/starred{/owner}{/repo}",
        subscriptions_url: "https://api.github.com/users/alan/subscriptions",
        organizations_url: "https://api.github.com/users/alan/orgs",
        repos_url: "https://api.github.com/users/alan/repos",
        events_url: "https://api.github.com/users/alan/events{/privacy}",
        received_events_url: "https://api.github.com/users/alan/received_events",
        type: "User",
        site_admin: false,
        name: "Alan Kennedy",
        company: "Duffel",
        blog: "",
        location: "London",
        email: null,
        hireable: null,
        bio: null,
        twitter_username: null,
        public_repos: 24,
        public_gists: 7,
        followers: 34,
        following: 23,
        created_at: "2008-04-10T22:51:31Z",
        updated_at: "2021-06-23T16:17:29Z"
        },
        {
        login: "justy",
        id: 210422,
        node_id: "MDQ6VXNlcjIxMDQyMg==",
        avatar_url: "https://avatars.githubusercontent.com/u/210422?v=4",
        gravatar_id: "",
        url: "https://api.github.com/users/justy",
        html_url: "https://github.com/justy",
        followers_url: "https://api.github.com/users/justy/followers",
        following_url: "https://api.github.com/users/justy/following{/other_user}",
        gists_url: "https://api.github.com/users/justy/gists{/gist_id}",
        starred_url: "https://api.github.com/users/justy/starred{/owner}{/repo}",
        subscriptions_url: "https://api.github.com/users/justy/subscriptions",
        organizations_url: "https://api.github.com/users/justy/orgs",
        repos_url: "https://api.github.com/users/justy/repos",
        events_url: "https://api.github.com/users/justy/events{/privacy}",
        received_events_url: "https://api.github.com/users/justy/received_events",
        type: "User",
        site_admin: false,
        name: "Justy",
        company: "Cool Fusion",
        blog: "http://justy.me",
        location: "Sydney, Australia",
        email: null,
        hireable: true,
        bio: "Full Stack Polymath, preferring Javascript, C, HTML, Node.js",
        twitter_username: null,
        public_repos: 24,
        public_gists: 11,
        followers: 25,
        following: 39,
        created_at: "2010-02-25T04:12:22Z",
        updated_at: "2021-11-05T21:17:00Z"
        }
      ]
  }
  },
  methods: {
    openCard: function(userInfo) {
      this.userCard = userInfo
    }
  },
  components: {
    UserCard,
    UserList
  }
}
</script>


