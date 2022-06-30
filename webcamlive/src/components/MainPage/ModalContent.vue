<template>
  <div id="start-box">
    <div class="start-input">
      <p>닉네임</p>
      <input type="text">
    </div>
    <div class="start-input">
      <p>방송 제목</p>
      <input type="text">
    </div>
    <div class="content-input">
      <p>방송 내용</p>
      <textarea></textarea>
    </div>
    <div class="buttons">
      <button @click="startLive" class="start-btn">방송 시작하기</button>
      <button @click="$emit('close')">닫기</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ModalContent",
  methods: {
  }
}

</script>

<style scope>
.start-input {
  display: flex;
  margin: 20px;
  align-items: baseline;
}

.start-input p,
.content-input p {
  width: 100px;
  text-align: start;
}

.start-input input {
  height: 2rem;
  width: 100%;
  border: none;
  outline: none;
  border-bottom: solid 2px;
}

.content-input {
  display: flex;
  flex-direction: column;
  margin: 20px;
  align-items: flex-start;
}

.content-input textarea {
  border: solid 2px;
  width: 100%;
  height:200px;
  border-radius: 10px;
  padding: 10px;
}

.content-input textarea:focus {
  outline: none;
}

.buttons button{
  outline: none;
  border: solid 2px black;
  border-radius: 10px;
  margin-left: .5rem;
  background: white;
}

.buttons button:nth-child(1) {
  background: black;
  color: white;
  transition: .3s;
}

.buttons button:nth-child(1):hover {
  transform: scale(1.1);
  box-shadow: 0px 3px rgb(129, 129, 129);
}

</style>