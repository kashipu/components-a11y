<template>
<nav class="border">
    <div class="container">
        <ul class="nav--principal" title="Principal" aria-label="Menú principal">
            <li class="nav--category" v-for="(title, index) in clasification" :key="index" tabindex="0">
            <p>{{title.name}}</p><small>{{title.summ}}</small>
            <div class="anidamiento--box" v-if="title.display">
                <ul class="nav--anidado" tabindex="0">
                    <li>Afiliaciones caja</li>
                    <li>Como independiente</li>
                    <li>Como contratista</li>  
                    <li>Como pensionado</li>
                    <li>Mi grupo familiar</li>
                </ul>
            </div>
            </li>
        </ul>
    </div>
</nav>
</template>

<script>
export default {
    data() {
        return {
        title: "Hola mundo",
        clasification: [
            {name: "Persona", summ:"Afiliación y Servicios de Caja", display:true},
            {name: "Empresa", summ:"Todo sobre empleadores", display:false},
            {name: "Salud", summ:"EPS y Plan Complementario", display:false},
            {name: "Sobre Compensar", summ:"Información Institucional", display:false}
        ],
        itemsClasificacion:[
            {class:"Persona",
            bussiness: "Afiliaciones Caja",
            subitems: [
                "1", "2", "3", "4" 
            ]}
        ]
        }
    }
}
</script>

<style scoped>
nav {
    background-color: var(--light-gray);
}
.nav--principal {
    display: flex;
    gap: 1rem;
    list-style: none;
    position: relative;
    margin-bottom: 0;
}

.nav--category {
    padding: .4rem 1rem;
}
.nav--principal li p {
    padding: 0;
    margin: 0;
    font-weight: var(--bold);
    text-transform: uppercase;
    line-height: 1.5;
}

.nav--principal li small {
    font-weight: var(--light);
    font-size: .9rem;
}

.anidamiento--box {
    position: absolute;
    margin-top: 8px;
    width: 100%;
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-auto-rows: repeat(3, 1fr);
    padding: 1rem 1.5rem;
    background-color: rgba(240, 240, 240, 0.8);
    width: 100%;
}

.nav--anidado {
    list-style: none;
    padding: 0em;
}
.nav--anidado li {
    font-weight: var(--light);
    font-size: .9rem;
}
.nav--anidado li:first-child {
    font-weight: var(--bold);
}





</style>