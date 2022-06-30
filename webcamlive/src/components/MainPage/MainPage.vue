<template>
  <div id="start-vue">
    <div id="start-box">
      <button @click="openModal">방송 시작하기</button>
    </div>
    <div id="live-list-box">
      <ul class="list-group">
        <LiveItem v-for="(live, idx) in lives" :key="idx" :live="live" />
      </ul>
    </div>
    <div>
      <StartModal v-if="modal" @close="closeModal">
        <ModalContent @close="closeModal" />
      </StartModal>
    </div>
  </div>
</template>

<script>
import StartModal from "@/components/MainPage/StartModal.vue"
import ModalContent from "@/components/MainPage/ModalContent.vue"
import LiveItem from "@/components/MainPage/LiveItem.vue"


export default {
  name: 'MainPage',
  components: {
    StartModal,
    LiveItem,
    ModalContent
  },
  data: function () {
    return {
      modal : false,
      lives: [
        {
          username: "일번",
          title: "일번 제목",
        },
        {
          username: "이번",
          title: "이번 제목",
        }
      ]
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
#start-vue {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#start-box button {
  outline: none;
  border: solid 2px black;
  border-radius: 10px;
  background: black;
  color: white;
  transition: .3s;
}

#start-box button:hover {
  transform: scale(1.1);
  box-shadow: 0px 3px rgb(129, 129, 129);
}

#live-list-box {
  width: 400px;
  margin-top: 2rem;
}

.list-group {
  width: 100%;
  outline: solid 2px black;
}
</style>

