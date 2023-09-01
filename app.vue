<template>
  <section>
    <div class="odocs-spaced">
      <button @click="imageModal()">Open modal (SimpleImage)</button>
      <button @click="cardModal()">Open modal (SimpleText)</button>
    </div>
  </section>
</template>

<script setup>
import SimpleText from '@/components/example/SimpleText.vue';
import SimpleImage from '@/components/example/SimpleImage.vue';

const { neoModal } = useProgrammatic();

function imageModal() {
  neoModal.closeAll();

  neoModal.open({
    component: SimpleImage,
    trapFocus: true,
  });
}

function cardModal() {
  neoModal.closeAll();

  neoModal.open({
    component: SimpleText,
    trapFocus: true,
  });
}
</script>
