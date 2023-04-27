<template>
    <div class="content" id="divpadre">
        <div id="superior">
            <div class="row medio">
                <div class="col-md-8 col-12">
                    <h2>Bienvenidos al curso:</h2>
                    <h1>Emprendedores y emprendimiento del salvador y la region</h1>
                </div>
                <div class="col-md-4 col-12 centrar">
                    <button class="circulo" id="botonocultar" @click="ocultarDiv"> </button>
                </div>
            </div>
        </div>
        <div id="inferior"> </div>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 319">
            <path fill="#FFFFFF" fill-opacity="1"
                d="M0,160L360,288L720,160L1080,64L1440,96L1440,320L1080,320L720,320L360,320L0,320Z"></path>
        </svg>
    </div>
</template>

<style>
.circulo {
    background-image: url('../assets/bitmap.svg');
    background-size: cover;
    width: 105px;
    height: 105px;
    border-radius: 50%;
    border: none;
    background-color: transparent;
}

.centrar {
    text-align: center;
}

.content {
    background-color: #086c34;
    transition: opacity 1s ease-in-out;
}

#superior {
    width: 100%;
    height: 80%;
    background-color: #086c34;
}
=
#inferior {
    width: 100%;
    height: 20%;
    background-color: white;
}

.medio {
    text-align: left;
    padding-top: 10%;
    padding-left: 10%;
}

.medio h1 {
    color: white;
    font-weight: bold;
}

.medio h2 {
    color: #0ba21a
}

.content svg {
    display: block;
}

.ocultar {
    opacity: 0;
    visibility: hidden;
    
}
</style>

<script>
export default {
    name: 'InicioBienvenida',
    data() {
        return {
            vista: false
        }
    },
    methods: {
        ocultarDiv() {
            var div = document.getElementById("divpadre");
            div.style.opacity = "0";
            div.style.pointerEvents = "none";
            this.vista = true
            this.$emit('mostrarDiv', this.vista)
            setTimeout(() => {
            div.style.display= 'none'    
            }, 1000);
        }
    }
}
</script>
