<template>
    <div v-if="isOpen" class="voluntierModal" @click.self="closeModal">
        <div class="flex-c ai-c gap-20 modalContent">
            <h1 class="txt-c" style="color: #4cced0;">¡Súmate a la Investigación Cerebral!</h1>
            <p class="txt-c" style="color: rgb(217, 217, 217); font-size: 14px;">El estudio dura solo ~2 horas, y tu colaboración es
                invaluable.</p>
            <p class="txt-jc">¡Gracias por tu interés en apoyar la investigación en la BUAP! Tu participación es
                fundamental para
                avanzar en nuestro estudio sobre pulsos binaurales y la activación cerebral, sentando bases para
                entender mejor condiciones como la esquizofrenia.</p>
            
            <p class="txt-jc" style="color: rgb(217, 217, 217); font-size: 14px;">Para garantizar la calidad de los datos, te pedimos no
                usar joyería ni productos en el cabello el día de tu visita, y evitar estimulantes como el café.</p>
            <a href="https://wa.me/522481557141" class="btn-1" target="_blank">¿Listo para Unirte? Envíanos un Mensaje</a>
            <p class="txt-jc" style="color: rgb(217, 217, 217); font-size: 14px;">¡Tu tiempo y disposición hacen la diferencia en la ciencia! Gracias por considerar ser parte de este importante proyecto.</p>
        </div>
    </div>
</template>
<script setup>
import { defineProps, defineEmits, watch } from 'vue';

// Define las props que recibirá el componente
const props = defineProps({
    isOpen: {
        type: Boolean,
        default: false
    }
});
const emit = defineEmits(['close']);
const closeModal = () => {
    emit('close'); // Emite un evento para que el componente padre cierre el modal
};

watch(() => props.isOpen, (newValue) => {
    if (newValue) {
        document.body.style.overflow = 'hidden'; // Evita el scroll cuando el modal está abierto
    } else {
        document.body.style.overflow = ''; // Restaura el scroll cuando el modal está cerrado
    }
}, { immediate: true });
document.addEventListener('keydown', (event) => {
    if (event.key === 'Escape' && props.isOpen) {
        closeModal();
    }
});
</script>