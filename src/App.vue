<template>
  <div id="App">
    <div class="container">
    <game-list :games="games" />
    <player-card :player="playerCard"
    v-if="playerCard" />
    <player-list 
    :players="players"
    :player="playerCard"
    @openCard="openCard"/>
    </div>
  </div>
</template>

<script>
import PlayerCard from '@/components/PlayerCard'
import PlayerList from './components/PlayerList.vue'
import GameList from './components/GameList.vue'


export default {
  name: 'App',
  data() {
    return {
      playerCard:'',
      players: []
  }
  },
  methods: {
    openCard: function(playerInfo) {
      this.playerCard = playerInfo
    }
  },
  components: {
    PlayerCard,
    PlayerList,
    GameList
  }
}
</script>


