<template>
    <div>
        <Voluntier :is-open="openModalVoluntier" @close="toggleModalVoluntier"></Voluntier>
    </div>
    <header class="main-section flex-c ai-c jc-c cont-10">
        <section class="flex-c ai-c gap-20 cont-8">
            <h1 class="txt-c color-w"> <span>Únete a la Ciencia:</span><br> Explora el Cerebro</h1>
            <h2 class="txt-jc color-bone">Sé parte de un estudio pionero sobre la activación cerebral con pulsos
                binaurales.</h2>
            <p class="txt-jc " style="color: #d9d9d9;">En el Instituto de Fisiología de la BUAP, estudiamos cómo el
                cerebro percibe los pulsos binaurales. Tu
                participación es clave para entender la función cerebral y sentar bases para investigar patologías como
                la esquizofrenia. ¡Tu tiempo impulsa la ciencia!</p>
            <div>
                <button @click="toggleModalVoluntier" class="btn-1">Deseo Participar</button>
            </div>
        </section>
    </header>


    <main class="flex-c ai-c cont-10">
        <section class="flex-c gap-40 cont-8">
            <article class="flex-c gap-20">
                <h2 class="txt-c"> ¿Qué Investigamos y Por Qué?</h2>
                <p class="txt-jc">En la BUAP, investigamos los pulsos binaurales: sonidos que tu cerebro procesa gracias
                    a una vía auditiva íntegra. Nuestro objetivo es identificar las áreas del cerebro que se activan con
                    estos pulsos. Esta investigación es crucial, ya que nos permitirá comparar estos hallazgos con
                    participantes con esquizofrenia en el futuro. También incluimos una prueba cognitiva.</p>
            </article>
            <article class="flex-c gap-20">
                <h2 class="txt-c"> ¿Cómo Puedes Participar?</h2>
                <p class="txt-jc">Tu colaboración es sencilla y segura. El estudio dura aproximadamente 2 horas,
                    principalmente por la colocación de electrodos EEG (un proceso no invasivo para registrar tu
                    actividad cerebral). Los pulsos binaurales se escuchan con audífonos.</p>
                <p class="txt-jc">Tu seguridad es nuestra prioridad: Es un procedimiento no invasivo y sin efectos adversos. Firmarás
                    un consentimiento informado.</p>
                <p class="txt-jc">Flexibilidad de horario: Nos adaptamos a tu disponibilidad.</p>
                <p class="txt-jc">Resultados: Si lo deseas, compartiremos los resultados de tu participación o el paper del estudio.
                </p>
            </article>
            <article class="flex-c gap-20">
                <h2 class="txt-c"> Antes del Estudio: Tu Preparación</h2>
                <p class="txt-jc">Para asegurar la mejor calidad de datos, te pedimos lo siguiente para el día de la prueba:"</p>
                <ul>
                    <li>Sin joyería: Aretes, collares, piercings, etc.</li>
                    <li>Cabello natural: Solo shampoo, sin otros productos.</li>
                    <li>Evita maquillaje: En lo posible.</li>
                    <li>Sin estimulantes: No café, bebidas energéticas u otras sustancias el día del estudio.</li>
                </ul>
                <p class="txt-c">¡Gracias por tu apoyo! Esto es crucial para la investigación!</p>
            </article>
            <hr style="width: 100%;">
            <article class="flex-c ai-c">
                <h4>Sitio Elaborado por</h4>
                <h3 style="margin-bottom: 10px;">Yohary Diaz Jimenez</h3>
                <a href="https://resume-yohary-diaz.vercel.app/" target="_blank">Más Información</a>
            </article>
        </section>
    </main>
</template>
<script setup>
import { ref } from 'vue';
import Voluntier from '@/components/Voluntier.vue';
const openModalVoluntier = ref(false);
const toggleModalVoluntier = ref(() => {
    console.log('hola')
    openModalVoluntier.value = !openModalVoluntier.value;
})
//
</script>