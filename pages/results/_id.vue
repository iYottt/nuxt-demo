<template>
    <div>
        <h1>Result: {{ $route.params.id }}</h1>
        <div v-if="albumExists">
            <div v-for="(album, index) in albumData" :key="index">
                <card
                    :image="album.artworkUrl100"
                    :title="album.collectionCensoredName"
                    :artistName="album.artistName"
                    :url="album.artistViewUrl"
                    :color="picker(index)"
                />
            </div>
        {{albumData}}
        </div>
        <div v-else>
            <h2>Not Found</h2>
        </div>
    </div>
</template>

<script>
import Axios from 'axios'
import Card from '@/components/Card.vue'
export default {
    asyncData ({params}) {
        return Axios.get('https://itunes.apple.com/search?term='+params.id+'&entity=album')
            .then( (response) => {
                return {albumData: response.data.results}
            });
    },
    components: {
        Card
    },
    middleware: 'search',
    methods: {
        picker (index) {
            return index % 2 == 0 ? 'red' : 'blue'
        }
    },
    computed: {
        albumExists() {
            return this.albumData.length > 0
        }
    }
}
</script>

