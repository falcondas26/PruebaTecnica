<template>

        <div >
            <div class="container">
        <div class="row">
            <div class="col-12">
            <h3>¿Que aprendiste durante este recorrido?</h3>
            <div>
                Para saberlo, te proponemos un breve ejercicio que te permitirá
                revisar los conceptos básicos vistos durante el curso. Arrastra las
                imágenes-concepto de la izquierda a la frase correspondiente de la
                derecha. ¡Buena suerte!
            </div>
            </div>
        </div>
        <div class="row">
            <div class="col-1"></div>
            <div class="col-5">
            <div class="col-12"  draggable="true"     id="pareja1">
                <div class="row align-items-center justify-content-center ">
                    <div class="col">
                        <img
                        src="../assets/diapositiva-19-1.svg"
                        alt="No se pudo cargar la imagen"
                        width="100"
                        height="100"
                        />
                    </div>
                    <div class="col">
                        <h6>Capital semilla</h6>
                    </div>
                    </div>
            </div>
            <div class="col-12" draggable="true">
                <div class="row align-items-center justify-content-center">
                <div class="col">
                    <img
                    src="../assets/diapositiva-19-2.svg"
                    alt="No se pudo cargar la imagen"
                    width="100"
                    height="100"
                    />
                </div>
                <div class="col">
                    <h6>Emprendimiento dinamico</h6>
                </div>
                </div>
            </div>
            <div class="col-12" draggable="true">
                <div class="row align-items-center justify-content-center">
                <div class="col">
                    <img
                    src="../assets/diapositiva-19-3.svg"
                    alt="No se pudo cargar la imagen"
                    width="100"
                    height="100"
                    />
                </div>
                <div class="col">
                    <h6>Ecosistema de negocios</h6>
                </div>
                </div>
            </div>
            <div class="col-12" draggable="true">
                <div class="row align-items-center justify-content-center">
                <div class="col">
                    <img
                    src="../assets/diapositiva-19-4.svg"
                    alt="No se pudo cargar la imagen"
                    width="100"
                    height="100"
                    />
                </div>
                <div class="col">
                    <h6>Networkin</h6>
                </div>
                </div>
            </div>
            <div class="col-12" draggable="true">
                <div class="row align-items-center justify-content-center">
                <div class="col">
                    <img
                    src="../assets/diapositiva-19-5.svg"
                    alt="No se pudo cargar la imagen"
                    width="100"
                    height="100"
                    />
                </div>
                <div class="col">
                    <h6>Acelerador de negocios</h6>
                </div>
                </div>
            </div>
            <div class="col-12" draggable="true"> 
                <div class="row align-items-center justify-content-center">
                <div class="col">
                    <img
                    src="../assets/diapositiva-19-6.svg"
                    alt="No se pudo cargar la imagen"
                    width="100"
                    height="100"
                    />
                </div>
                <div class="col">
                    <h6>Red de angeles inversos</h6>
                </div>
                </div>
            </div>
            </div>
            <div class="col-5">
                <div class="row gy-5">
                    <div class="col-12" id="contenedor1">
                        <div class="row gy-10 align-items-center justify-content-center">
                        <div class="form-check-input col-2" type="checkbox"></div>
                        <div class="col-10">
                            Financiación que se emplea para necesidades específicas del
                            negocio (prototipos, investigación de mercado, producción
                            inicial, etc.)
                        </div>
                        </div>
                    </div>
                    <div class="col-12" id="contenedor2">
                        <div class="row align-items-center justify-content-center">
                        <div class="form-check-input col-2" type="checkbox"></div>
                        <div class="col-10">
                            Proyecto con potencial de crecer de manera rentable, rápida y sostenible, que genera valor agregado y tiene ventajas competitivas.
                        </div>
                        </div>
                    </div>
                    <div class="col-12" id="contenedor3">
                        <div class="row align-items-center justify-content-center ">
                        <div class="form-check-input col-2" type="checkbox"></div>
                        <div class="col-10">
                            Comunidad conformada por individuos y organizaciones con el objetivo de producir bienes y servicios de valor a quienes hacen parte de ella.
                        </div>
                        </div>
                    </div>
                    <div class="col-12" id="contenedor4">
                        <div class="row align-items-center justify-content-center ">
                        <div class="form-check-input col-2" type="checkbox"></div>
                        <div class="col-10">
                            Red de contactos que se conforma con el objetivo de iniciar una relación de negocios o de intercambio de conocimiento.
                        </div>
                        </div>
                    </div>
                    <div class="col-12" id="contenedor5">
                        <div class="row align-items-center justify-content-center ">
                        <div class="form-check-input col-2" type="checkbox"></div>
                        <div class="col-10">
                            Organización que impulsa a los negocios a convertirse en empresas dinámicas y de alto crecimiento.
                        </div>
                        </div>
                    </div>
                    <div class="col-12" id="contenedor6">
                        <div class="row align-items-center justify-content-center ">
                        <div class="form-check-input col-2" type="checkbox"></div>
                        <div class="col-10">
                            Un colectivo de individuos con recursos y de probada experiencia empresarial que colaboran, como grupo, en la selección, inversión, involucramiento y apoyo de emprendimientos dinámicos en alianza con el emprendedor.
                        </div>
                        </div>
                    </div>

                </div>
            
            </div>
            <div class="col-1"></div>
        </div>
        </div>
















        
    </div>


</template>



<style>
#contenedor{
    width: 200px;
    height: 200px;
    border: 1px solid black;
}
#cajap{
    width: 100px;
    height: 100px;
    border: 1px solid black;
}


</style>
<script>   
export default {
    name: 'DragDrop',
    methods:{
        Inicio(e){
            const elementoArrastrado = e.target;
            const idArrastrado = elementoArrastrado.getAttribute('id');
            e.dataTransfer.setData('text/plain', idArrastrado);
        },
        Agregar(e){
            
            const ida = e.dataTransfer.getData('text/plain');
            console.log(ida)
            if(ida !== 'pareja1'){
                e.preventDefault();
            }else{
                e.target.appendChild(document.getElementById('pareja1'))
            }
            
        }
    },
    mounted(){
        document.getElementById('contenedor1').addEventListener('dragstart',(e) => { this.Inicio(e);console.log("Dragov")});
        document.getElementById('contenedor1').addEventListener('dragover',(e) => { e.preventDefault();console.log("Dragov")});
        
        document.getElementById('contenedor1').addEventListener('drop',(e) => { this.Agregar(e,this.contenedor1) ;console.log("Dragovd")});
        document.getElementById('contenedor2').addEventListener('dragenter',() => { console.log("Drag")});
        document.getElementById('contenedor3').addEventListener('dragenter',() => { console.log("Drag")});
        document.getElementById('contenedor4').addEventListener('dragenter',() => { console.log("Drag")});
        document.getElementById('contenedor5').addEventListener('dragenter',() => { console.log("Drag")});
        document.getElementById('contenedor6').addEventListener('dragenter',() => { console.log("Drag")});
    }
}
</script>
