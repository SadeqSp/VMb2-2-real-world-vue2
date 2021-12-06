<template>
    <div>
        <h1>event list</h1>
        <EventCard v-for="event in events" :key="event.id" :event="event" />
    </div>
</template>

<script>
    import EventCard from '@/components/EventCard.vue';
    import EventService from '@/services/EventService.js'

    export default {
        data() {
            return {
                events: []
            }
        },
        components: {
            EventCard
        },
        created() {
            EventService.getEvents()
                        .then( response => { this.events = response.data })
                        .catch( error => { console.log(error) })
        }
    };
</script>