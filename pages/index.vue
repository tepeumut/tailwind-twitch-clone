<template>
  <div class="flex flex-grow">
    <div class="flex flex-col flex-grow">
      <div class="player">
        <iframe
          src="https://player.twitch.tv/?channel=asd&parent=localhost"
          height="759px"
          width="99%"
        >
        </iframe>
      </div>
      <div class="stream-card">
        <div class="stream-info">
          <div class="streamer-avatar">
            <img class="w-20 rounded-full"
                 src="https://static-cdn.jtvnw.net/jtv_user_pictures/d9654b94-4d5e-4033-a418-23feec57e484-profile_image-70x70.png"
                 alt="">
          </div>
          <div class="streamer-info">
            <div class="streamer-name">
              tepeumut
            </div>
            <div class="streamer-stream-title">
              chill mode on
            </div>
            <div class="streamer-game-badge">
              <div class="game-badge">
                Just Chatting
              </div>
              <div class="streamer-badge">Turkish</div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="right-side">
      coming soon... :)
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style>
.player {
  @apply
  w-full
}

.right-side {
  @apply
  w-80
}

.stream-card {
  @apply
  mt-4
  ml-3
}

.streamer-avatar {
  @apply
  mt-2
  pl-2
}

.stream-info {
  @apply
  flex flex-row
}

.streamer-info {
  @apply
  flex flex-col justify-center
  ml-2
}

.streamer-name {
  @apply
  font-semibold
  text-xl
}

.streamer-stream-title {
  @apply
  font-semibold
  text-sm
}

.streamer-game-badge {
  @apply
  flex flex-row items-center
  space-x-3
}

.game-badge {
  @apply
  text-purple-600
}

.streamer-badge {
  @apply
  flex items-center
  text-xs
  bg-gray-200
  rounded-full
  px-2
  text-gray-500
  font-semibold
  h-4

  hover:bg-gray-300
}

</style>
