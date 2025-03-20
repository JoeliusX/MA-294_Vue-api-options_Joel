<template>
  <div class="events" v-for="event in events" :key="event.id">
    <EventCard :event="event" />
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from '@/components/EventCard.vue'

export default {
  name: 'HomeView',
  data() {
    return {
      events: [
        {
          id: 11101,
          category: 'Promotion',
          title: 'Portes ouvertes',
          description: 'Présentation des activités de la filière au public.',
          location: 'Nos locaux',
          date: '25 novembre 2024',
          time: '08:00',
        },
        {
          id: 20201,
          category: 'Loisirs',
          title: 'Journéé ski',
          description:
            'Activité neige dans Ste-Croix et à la station des Rasses pour du ski de fond, ski de descente et randonnée.',
          location: 'Ste-Croix',
          date: '14 février 2025',
          time: '08:30',
        },
        {
          id: 30901,
          category: 'Loisirs',
          title: 'Semaine spéciale',
          description:
            "Voyage à l' étranger avec des activités proposées par les élèves.",
          location: 'Étranger',
          date: 'Septembre 2025',
          time: '06:00',
        },
      ],
    }
  },
  components: {
    EventCard,
  },
}
</script>

<style>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
