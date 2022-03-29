<script>
    import { onMount } from 'svelte';

    let data = [];
    let results = [];
    const API = "https://kittygram-api.now.sh/"

    onMount(async () => {
        const response = await fetch(API);
        let result = await response.json();
        results = result.posts;
        data = results;
        console.log('results:',results);
    });

    /* scroll configuration */
        let page = 0; 
        let size = 3;

        function prueba(){
            console.log('hola')
        }
    /* ----- */

</script>

<main>
    <section class="banner">
        <div class="title-container">
            <h1 class="landing-title">
                La herramienta para la coordinación
                <br>
                de equipos de abogados
            </h1>
            <h2 class="landing-subtitle">Jude es la plataforma donde puedes coordinarte con tu equipo y controlar la información de forma segura.</h2>
        </div>
    </section>
    
    <section class="secure-data">
        <div class="section-container">
            <div class="left-side">
                <div class="secure-text-container">
                    <h2 class="secure-data-title">Información protegida</h2>
                    <p class="secure-data-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem ipsum dolore dolorum libero accusamus nam ipsa magnam, porro totam, officiis praesentium neque non ea laborum doloribus ratione expedita ut repudiandae!</p>
                </div>
            </div>
            <div class="right-side">
                <div class="secure-image-container">
                    <img class="secure-image" alt="hola" src="https://thumb.tildacdn.com/tild3530-3664-4539-a431-376164633937/-/resize/800x/-/format/webp/li3x.png">
                </div>
            </div>
        </div>
    </section>

    <section class="secure-files">
        <div class="title-section">
            <h1 class="title">Coordinación de Equipos</h1>
            <h2 class="subtitle">Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem ipsum dolore dolorum <br>  libero accusamus nam ipsa magnam, porro totam, officiis praesentium <br> neque non ea laborum doloribus ratione expedita ut repudiandae!.</h2>
        </div>
        <div class="section-container">
            <div class="right-side">
                <div class="secure-image-container">
                    <img class="secure-image" alt="hola" src="https://thumb.tildacdn.com/tild3863-3733-4264-a335-393236333666/-/resize/800x/-/format/webp/retail-customer3x.png">
                </div>
            </div>
            <div class="left-side">
                <div class="secure-text-container">
                    <h2 class="secure-data-title">Acelera grupos de trabajo</h2>
                    <p class="secure-data-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem ipsum dolore dolorum libero accusamus nam ipsa magnam, porro totam, officiis praesentium neque non ea laborum doloribus ratione expedita ut repudiandae!.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="secure-data">
        <div class="section-container">
            <div class="left-side">
                <div class="secure-text-container">
                    <h2 class="secure-data-title">Comunicación con el Cliente</h2>
                    <p class="secure-data-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem ipsum dolore dolorum libero accusamus nam ipsa magnam, porro totam, officiis praesentium neque non ea laborum doloribus ratione expedita ut repudiandae!.</p>
                </div>
            </div>
            <div class="right-side">
                <div class="secure-image-container">
                    <img class="secure-image" alt="hola" src="https://thumb.tildacdn.com/tild3836-3837-4836-b366-306134363431/-/resize/800x/-/format/webp/campaign-management3.png">
                </div>
            </div>
        </div>
    </section>

    <section class="secure-data">
        <div class="section-container">
            <div class="right-side">
                <div class="secure-image-container">
                    <img class="secure-image" alt="hola" src="https://thumb.tildacdn.com/tild3066-3739-4130-a464-376636343433/-/resize/800x/-/format/webp/platform-image3x.png">
                </div>
            </div>
            <div class="left-side">
                <div class="secure-text-container">
                    <h2 class="secure-data-title">Tracking de la información</h2>
                    <p class="secure-data-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem ipsum dolore dolorum libero accusamus nam ipsa magnam, porro totam, officiis praesentium neque non ea laborum doloribus ratione expedita ut repudiandae!.</p>
                </div>
            </div>
        </div>
    </section>
</main>

<style>

/* Banner */

.banner{
    min-height: 100vh;
    max-height: 100vh;
    width: 100vw;
    background: url("https://rabbit.io/landing/images/illustration-head.svg");
    background-repeat: no-repeat;
    background-size: cover;
    background-color: #09194B;
}

.title-container{
    padding-top: 14%;
}

.landing-title{
    font-size: 4rem;
    font-weight: 600;
    text-align: center;
    margin-top: 0%;
    color: #FFFFFF;
}

.landing-subtitle{
    margin-top: 0%;
    text-align: center;
    color: #FFFFFF; 
    font-size: 1.125rem;
    font-weight: 400;
    line-height: 1.78em;
    margin-bottom: 2rem;
}

/* */
.secure-files{
    min-height: 120vh;
    max-height: 120vh;
    padding-top: 10vh;
    padding-bottom: 10vh;
    background: #F0F4F4;
}

.title{
    font-size: 3rem;
    font-weight: 600;
    text-align: center;
}

.subtitle{
    font-weight: 400;
    font-size: 1.125rem;
    line-height: 1.78em;
    text-align: center;
}


/* Secure Data  */

.secure-data{
    min-height: 100vh;
    max-height: 100vh;  
}

.section-container{
    display: flex;
}

/* */
    
.left-side{
    width: 100%;
    min-height: 100vh;
    max-height: 100vh;
}

.secure-text-container{
    width: 70%;
    margin-left: 20%;
    padding-top: 30%;
}

.secure-data-title{
    font-size: 3rem;
    font-weight: 700;
    line-height: 1.2em;
}

.secure-data-text{
    font-weight: 400;
    font-size: 1.125rem;
    line-height: 1.78em;
}

/* */

.right-side{
    width: 100%;
    min-height: 100vh;
    max-height: 100vh;
}

.secure-image-container{
    padding-top: 15%;
}

.secure-image{
    max-width: 45vw;
    height: 45vw;
    float: right;
    border-radius: 10px;
}

/* */

.card{
    width: 50%;
    margin-left: 25%;
    display: flex;
    padding-top: 2%;
    padding-bottom: 2%;
}

/* parte izquierda */

.card-date{
    width: 15%;
}

.text-date{
    text-align: right;
    color: #b5babe;
    font-size: .9rem;
    margin: 0%;
}

/* parte derecha */

.card-content{
    width: 65%;
    margin-left: 5%;
    border-bottom: 1px solid #f3f3f3;
}

.title-content{
    font-size: 1.55rem;
    font-weight: 500;
    padding: 0%;
    margin: 0%;
}

.bag-container{
    margin-top: 15px;
    height: 20px;
}

.bag{
    background: #82afec;
    color: white;
    font-size: 12px;
    padding: 5px 9px 5px 9px;
    border-radius: 10px;
}
/*
.description-content{
    line-height: 1.55rem;
}
*/
</style>