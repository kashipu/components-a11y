<template>
    <a class="skip__link" href="#main" tabindex="0">Llevar al contenido principal</a>
</template>

<style>
.skip__link {
    display: flex;
    justify-content: center;
    border: 1px dotted var(--black-text);
    padding: .2rem 2rem;
    position: absolute;
    top: -35px;
    text-decoration: none;
}

.skip__link:focus,
.skip__link:active {
    top: 0;
}
</style>