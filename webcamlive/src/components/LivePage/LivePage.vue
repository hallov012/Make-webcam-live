<template>
  <section id="live-box">
    <div id="video-box">
    </div>
    <div id="host-box">
    </div>
    <div id="chat-box">
    </div>
  </section>
</template>

<script>
export default {
  name: "LivePage"
}
</script>

<style>
#live-box {
  border: solid 2px black;
  border-radius: 20px;
  width: 80vw;
  margin: auto;
  height: 85vh;
}

#video-box {
  height: 60%;
  border-bottom: solid 2px black;
}

#host-box {
  width: 40%;
  height: 40%;
  border-right: solid 2px black;
}

#chat-box {
  width: 60%;
  height: 40%;
  position: relative;
  bottom: 40%;
  left: 40%;
}

@media (min-width: 1300px) {
  #video-box {
    width: 70%;
    border-right: solid 2px black;
  }

  #host-box {
    width: 70%;
  }

  #chat-box {
    width: 30%;
    height: 100%;
    bottom: 100%;
    left: 70%;
  }
}
</style>