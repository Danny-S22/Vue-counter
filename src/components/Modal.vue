<template>
    <div class="modal" v-show="modalActive">
        <div class="modal-content p-4" v-if="modalActive">
            <slot />
            <button class="btn btn-secondary btn-dark" @click="closeModal">Close</button>
        </div>
    </div>
</template>

<script setup>
import { defineEmits, defineProps } from 'vue';

const emit = defineEmits(['close-modal']);
const props = defineProps({
    modalActive: {
        type: Boolean,
        default: false
    }
});

const closeModal = () => {
    emit('close-modal');
};
</script>

<style scoped>
.modal {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;

}
.modal-content {
    background-color: white;
    border-radius: 5px;
    max-width: 30vw;
}
</style>