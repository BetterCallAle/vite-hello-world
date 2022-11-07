<script>
export default{
    data(){
        return{
            games: [{
                name: "It Takes Two",
                description: "It Takes Two è un videogioco platform action-adventure sviluppato da Hazelight Studios e pubblicato da Electronic Arts, con l'etichetta EA Originals",
                imgPath: this.takeImgPath("../assets/img/it-takes-two-hero-banner-desktop.jpg"),
                imgAlt: "Cover di It Takes Two",
            },
            {
                name: "Returnal",
                description: "Returnal è un videogioco di genere sparatutto in terza persona horror psicologico con elementi roguelike sviluppato da Housemarque e pubblicato da Sony Interactive Entertainment",
                imgPath:this.takeImgPath("../assets/img/returnal-listing-thumb-01-ps5.jpg"),
                imgAlt:"Cover di Returnal"
            }
        ],

        index: 0
        }
    },
    methods: {
        takeImgPath(pathImage){
            return new URL(pathImage, import.meta.url).href
        },

        startTimer(){
            setInterval(()=>{
                if(this.index < this.games.length -1){
                    this.index++;
                } else {
                    this.index = 0
                }
            }, 3000)
        }
    },

    created() {
        this.startTimer()
    }
}
</script>

<template>
    <div class="jumbo-wrapper">
        <div class="jumbo-img">
            <img :src="games[index].imgPath" :alt="games[index].imgAlt">
        </div>

        <div class="jumbo-info">
            <h2>{{ games[index].name }}</h2>
            <p>{{ games[index].description }}</p>
            <button><a href="#">Download</a></button>
        </div>
    </div>

    
</template>

<style scoped>
a{
    text-decoration: none;
    color: inherit;
}

img{
    max-width: 100%;
}
.jumbo-wrapper{
    position: relative;
}

.jumbo-img{
    width: 100%;
    max-height: 390px;
    overflow: hidden;
    border-radius: 10px;
}

.jumbo-info{
    width: 70%;
    color: white;
    position: absolute;
    top: 50%;
    left: 10px;
    transform: translateY(-50%);
}

.jumbo-info p{
    margin: 1rem 0;
    font-size: 1.2rem;
}

.jumbo-info button{
    color: white;
    background-color: transparent;
    border: 1px solid white;
    border-radius: 50px;
    padding: 1rem;
    cursor: pointer;
    transition: all 125ms linear;
}

.jumbo-info button:hover{
    background-color: white;
    color: black;
}
</style>