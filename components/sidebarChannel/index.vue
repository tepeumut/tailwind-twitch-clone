<template>
  <div class="channel">
    <div class="channel-avatar">
      <img class="w-10 rounded-full"
           src="https://static-cdn.jtvnw.net/jtv_user_pictures/d9654b94-4d5e-4033-a418-23feec57e484-profile_image-70x70.png"
           alt="">
    </div>
    <div class="channel-main">
      <div class="channel-detail">
        <div class="channel-name">
          tepeumut
        </div>
        <div class="channel-game">
          Just Chatting
        </div>
      </div>
      <div class="channel-status">
        <div class="channel-online" v-if="isOnline">
          <div class="online"></div>
          9.5k
        </div>
        <div v-else>
          Offline
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "sidebarChannel",
  props: {
    isOnline: Boolean
  }
}
</script>

<style scoped>
.channel {
  @apply
  flex flex-row
  justify-start
  py-1 pl-2 pr-3
  cursor-pointer

  hover:bg-gray-300
}

.channel-main {
  @apply
  flex flex-row justify-between
  items-start
  w-full
  ml-2
}

.channel-detail {
  @apply
  flex flex-col
  items-start
  text-gray-600
}

.channel-name {
  @apply
  leading-4
  text-black
  font-semibold
}

.channel-game {
  @apply
  leading-4
  text-sm
}

.channel-status {
  @apply
  text-sm
}

.channel-online {
  @apply
  flex flex-row
  justify-center items-center
}

.online {
  @apply
  w-2 h-2
  block
  rounded-full
  bg-red-600
  mr-1
}

</style>
