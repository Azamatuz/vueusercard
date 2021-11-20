<template>
<div>
        <div class='container text-center'>
        <h1>Sport Forcaster</h1>
        <h2>Games</h2>
        <table class="table" style="min-width: 600px;">
            <thead>
                <tr>
                    <th scope="col">Game</th>
                    <th scope="col">Date</th>
                    <!--<th scope="col">Boost</th>-->
                    <th scope="col">Score</th>
                    <!--<th scope="col">Score Sum</th>-->
                    <th>Actions</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="(event, index) in events" :key="index">
                    <td>{{ event['home-team'].name }}({{ event['home-team'].abbreviation }}) vs
                        {{ event['away-team'].name }}({{ event['away-team'].abbreviation }})</td>
                    <td>{{ event['event-date'] }} {{ event['event-time'] }}</td>
                    <td>{{ event['home-team']['actual-score'] }} - {{ event['away-team']['actual-score'] }}</td>
                    <td><button class="btn btn-primary btn-sm">Players</button>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</div>

</template>

<script>
    import axios from 'axios'

    export default {
        name: 'game-list',
        props: {},
        data() {
            return {
                events: null,
                eventSelected: null,
                errors: null
            }
        },
        created() {
            axios.get('http://localhost:3000/events')
                .then(res => {
                    this.events = res.data
                })
                .catch(e => {
                    this.errors.push(e)
                })
        }
    }
</script>