<template>
    <div>
        <h1>event list</h1>
        <EventCard />
    </div>
</template>

<script>
    import EventCard from '@/components/EventCard.vue';
    
    export default {
        components: {
            EventCard
        },
    };
</script>