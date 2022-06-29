<template>
  <div>
    <h2>Home</h2>
    <div id="start-box">
      <button @click="openModal">방송 시작하기</button>
    </div>
    <div>
      <StartModal v-if="modal" @close="closeModal">
        <ModalContent @close="closeModal" />
      </StartModal>
    </div>
  </div>
</template>

<script>
import StartModal from "@/components/StartModal.vue"
import ModalContent from "@/components/ModalContent.vue"

export default {
  name: 'MainPage',
  components: {
    StartModal,
    ModalContent
  },
  data: function () {
    return {
      modal : false
    }
  },
  methods: {
    openModal: function () {
      this.modal = true
      console.log(this.modal)
    },
    closeModal: function () {
      this.modal = false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

