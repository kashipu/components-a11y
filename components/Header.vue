<template>
    <header class="header">
        <div class="container">
            <div class="row py-2  d-flex align-items-center">
                <div class="col-md-2 d-flex justify-content-center" role="region" aria-label="Logo Compensar">
                    <a href="/">
                        <img width="148" height="41" src="https://corporativo.compensar.com/PublishingImages/logo_compensar.png" alt="Logo Compensar, lleva al inicio">
                    </a>
                </div>
                <div class="col-md-8 d-flex justify-content-center" role="region" aria-label="Buscador página">
                    <div class="search--items">
                        <label for="search">Buscar</label>
                        <input title="Buscador página" type="text" id="search" placeholder="¿Buscas algo?">
                        <button aria-label="Botón buscar en la página" class="btn search--button" type="submit"><i class="fas fa-search"></i></button>
                    </div>
                </div>
                <div class="col-md-2" role="region" aria-label="Botones transaccionales">
                    <ul class="buttons-grid">
                        <li>
                            <a href="#" aria-label="Tienda Compensar" class="button-transaccion">
                                <i class="fas fa-shopping-cart"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#" aria-label="Sedes Compensar" class="button-transaccion">
                                <i class="fas fa-map-marker-alt"></i>
                            </a>
                        </li>
                        <li>
                            <a href="#" aria-label="Ingreso a transacciones en línea" class="button-transaccion">
                                <i class="fas fa-user-circle"></i>
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <Navigation/>
    </header>
</template>

<script>
export default {

}
</script>

<style scoped>
/* Search Styles */
.search--items {
    position: relative;
    width: 60%;
}
.search--items label {
    display: none;
}
.search--items input {
    width: 100%;
    border: 1px solid var(--light-gray);
    border-radius: 1.5rem;
    padding-left: 1rem;
}
.search--items input::placeholder {
    color: var(--black-text);
    font-size: 0.7rem;
    font-weight: var(--light);
}
.search--button {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: var(--main-orange);
    width: 23px;
    height: 23px;
    border-radius: 50%;
    padding: 10px;
    position: absolute;
    top: 3px;
    right: 3px;
}
.search--button i {
    color: var(--white);
}
/* Buttons transaccion */
.buttons-grid {
    margin: 0;
    padding: 0;
    list-style: none;
    display: flex;
    gap: 1rem;
}
.button-transaccion {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: var(--light-gray);
    padding: 1rem;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    text-decoration: none;
}
.button-transaccion i {
    font-size: 1.25rem;
    color: var(--black-text);
}
</style>