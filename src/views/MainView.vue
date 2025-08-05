<template>
    <div>
        <Voluntier :is-open="openModalVoluntier" @close="toggleModalVoluntier"></Voluntier>
    </div>
    <header class="main-section flex-c ai-c jc-c cont-10">
        <section class="flex-c ai-c gap-20 cont-8">
            <p style="color: rgb(255, 251, 231);" class="txt-c fw-6">El Dr. Jorge Luis Calderón Garcia te invita a</p>
            <h1 class="txt-c color-w"> <span>Únete a la Ciencia:</span><br> Explora el Cerebro</h1>
            <p class="txt-jc fw-6" style="color: #000;">Ayúdanos a entender cómo el cerebro procesa los pulsos
                binaurales
                en el
                Instituto de Fisiología de la BUAP. Tu participación es clave para
                investigar patologías como la esquizofrenia.</p>
            <div>
                <button @click="toggleModalVoluntier" class="btn-1">Deseo Participar</button>
            </div>
        </section>
    </header>


    <main class="flex-c ai-c gap-20 cont-10">
        <section class="flex-c ai-c cont-10">
            <article class="flex-c gap-20 cont-8">
                <h2 class="txt-c color-hl"> ¿Qué Investigamos y Por Qué?</h2>
                <p class="txt-jc">En la BUAP, investigamos los <strong>pulsos binaurales</strong>: sonidos que tu
                    cerebro procesa gracias
                    a una vía auditiva íntegra. Nuestro objetivo es identificar las <strong>áreas del cerebro que se
                        activan</strong> con
                    estos pulsos. Esta investigación es crucial, ya que nos permitirá comparar estos hallazgos con
                    participantes con <strong>esquizofrenia</strong> en el futuro. También incluimos una <strong>prueba
                        cognitiva.</strong></p>
                <img src="/img/1.jpeg" alt="img">
            </article>
        </section>
        <section class="flex-c ai-c pv-20 cont-10" style="background-color: #f1f3fb;">

            <article class="flex-c gap-20 cont-8">
                <h2 class="txt-c color-hl"> ¿Cómo Puedes Participar?</h2>
                <p class="txt-jc">Tu colaboración es <strong>sencilla y segura.</strong> El estudio dura
                    <strong>aproximadamente 2 horas,</strong>
                    principalmente por la <strong>colocación de electrodos EEG</strong> (un proceso no invasivo para
                    registrar tu
                    actividad cerebral). Los pulsos binaurales se escuchan con <strong>audífonos.</strong>
                </p>
                <p class="txt-jc"><strong>Tu seguridad es nuestra prioridad:</strong> Es un procedimiento no invasivo y
                    sin efectos
                    adversos. Firmarás
                    un consentimiento informado.</p>
                <p class="txt-jc"><strong>Flexibilidad de horario:</strong> Nos adaptamos a tu disponibilidad.</p>
                <p class="txt-jc"><strong>Resultados:</strong> Si lo deseas, compartiremos los resultados de tu
                    participación o el paper
                    del estudio.
                </p>
                
                <img src="/img/2.jpeg" alt="img">
            </article>

        </section>

        <section class="flex-c ai-c pv-20 cont-10">
            <article class="flex-c cont-8 gap-20">
                <h2 class="txt-c  color-hl"> Antes del Estudio: Tu Preparación</h2>
                <p class="txt-jc">Para asegurar la mejor calidad de datos, te pedimos lo siguiente para el día de la
                    prueba:"</p>
                <ul style="margin-left: 10px;">
                    <li><strong>Sin joyería:</strong> Aretes, collares, piercings, etc.</li>
                    <li><strong>Cabello natural:</strong> Solo shampoo, sin otros productos.</li>
                    <li><strong>Evita maquillaje:</strong> En lo posible.</li>
                    <li><strong>Sin estimulantes:</strong> No café, bebidas energéticas u otras sustancias el día del
                        estudio.</li>
                </ul>
                <p class="txt-c"> <strong>¡Gracias por tu apoyo! Esto es crucial para la investigación!</strong></p>
            </article>

        </section>
    </main>
    <footer class="flex-c ai-c">
        <h4 class="color-bone">Sitio Elaborado por</h4>
        <h3 class="color-bone" style="margin-bottom: 10px;">Yohary Diaz Jimenez</h3>
        <a href="https://resume-yohary-diaz.vercel.app/" target="_blank">Más Información</a>
    </footer>
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