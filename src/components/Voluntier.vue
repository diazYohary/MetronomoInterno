<template>
    <div v-if="isOpen" class="voluntierModal" @click.self="closeModal">
        <div class="flex-c ai-c gap-20 modalContent">
            <h1 class="txt-c" style="color: #4cced0;">¡Súmate a Nuestra Investigación   !</h1>
            <p class="txt-jc">¡Gracias por tu interés en apoyar la investigación en la BUAP! Tu participación es
                fundamental para
                avanzar en nuestro estudio sobre pulsos binaurales y la activación cerebral, sentando bases para
                entender mejor condiciones como la esquizofrenia.</p>
            
            <p class="txt-jc" style="color: rgb(217, 217, 217); font-size: 14px;">
                <span>El estudio dura ~2 horas, es seguro y no invasivo.</span><br>
                Solo te pedimos evitar joyería, productos en el cabello y estimulantes el día de la prueba.
            </p>
            <a href="https://wa.me/522481557141" class="btn-1" target="_blank">¿Listo para Unirte? Envíanos un Mensaje</a>
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