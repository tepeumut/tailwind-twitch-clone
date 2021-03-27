<template>
  <div class="header">
    <div class="left-side h-full">
      <Logo class="mx-2"/>
      <NuxtLink class="nav-link" to="/following">Following</NuxtLink>
      <NuxtLink class="nav-link" to="/browse">Browse</NuxtLink>
      <div class="more-link">
        <svg class="h-5" viewBox="0 0 20 20" x="0px" y="0px">
          <g>
            <path
              d="M2 10a2 2 0 114 0 2 2 0 01-4 0zM8 10a2 2 0 114 0 2 2 0 01-4 0zM16 8a2 2 0 100 4 2 2 0 000-4z"></path>
          </g>
        </svg>
      </div>
    </div>
    <div class="search-box">
      <input type="text"
             placeholder="Search"
             class="search-input"/>
      <div class="search-icon">
        <svg class="w-6 h-6" viewBox="0 0 20 20" x="0px" y="0px">
          <g>
            <path fill-rule="evenodd"
                  d="M13.192 14.606a7 7 0 111.414-1.414l3.101 3.1-1.414 1.415-3.1-3.1zM14 9A5 5 0 114 9a5 5 0 0110 0z"
                  clip-rule="evenodd" fill="currentColor"></path>
          </g>
        </svg>
      </div>
    </div>
    <div class="right-side">
      <div class="right-nav-link">
        <svg class="h-5" viewBox="0 0 20 20" x="0px" y="0px">
          <g>
            <path fill-rule="evenodd" clip-rule="evenodd"
                  d="M13.798 10.456L10 6.657l-3.798 3.799L4 8.805V13h12V8.805l-2.202 1.65zM18 5v8a2 2 0 0 1-2 2H4a2.002 2.002 0 0 1-2-2V5l4 3 4-4 4 4 4-3z"></path>
          </g>
        </svg>
      </div>
      <div class="right-nav-link">
        <svg class="h-5" viewBox="0 0 20 20" x="0px" y="0px">
          <g>
            <path fill-rule="evenodd"
                  d="M4 3h12l2 4v10H2V7l2-4zm.236 4H8v1a1 1 0 001 1h2a1 1 0 001-1V7h3.764l-1-2H5.236l-1 2zM16 9h-2.17A3.001 3.001 0 0111 11H9a3.001 3.001 0 01-2.83-2H4v6h12V9z"
                  clip-rule="evenodd"></path>
          </g>
        </svg>
      </div>
      <div class="right-nav-link">
        <svg class="h-5" viewBox="0 0 20 20" x="0px" y="0px">
          <g>
            <path fill-rule="evenodd"
                  d="M7.828 13L10 15.172 12.172 13H15V5H5v8h2.828zM10 18l-3-3H5a2 2 0 01-2-2V5a2 2 0 012-2h10a2 2 0 012 2v8a2 2 0 01-2 2h-2l-3 3z"
                  clip-rule="evenodd"></path>
          </g>
        </svg>
      </div>
      <div class="get-bits-link">
        <svg class="h-5" viewBox="0 0 20 20" x="0px" y="0px">
          <path fill-rule="evenodd" clip-rule="evenodd"
                d="M3 12l7-10 7 10-7 6-7-6zm2.678-.338L10 5.487l4.322 6.173-.85.728L10 11l-3.473 1.39-.849-.729z"></path>
        </svg>
        Get Bits
      </div>
      <div class="avatar">
        <img class="rounded-full" src="https://static-cdn.jtvnw.net/jtv_user_pictures/d9654b94-4d5e-4033-a418-23feec57e484-profile_image-70x70.png" alt="">
        <div class="avatar-status">
          <div class="avatar-status-offline"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "index"
}
</script>

<style scoped>
.header {
  @apply
  flex flex-row justify-between
  items-center
  h-12
  shadow-md
}

.left-side {
  @apply
  flex items-center
  justify-start
}

.nav-link {
  @apply
  pl-4
  pr-4
  font-semibold
  flex items-center
  text-xl

  hover:text-purple-600
}

.more-link {
  @apply
  ml-4
  p-1
  rounded
  cursor-pointer
  flex justify-center items-center
  hover:bg-gray-200
}

.search-box {
  @apply
  flex flex-row
}

.search-input {
  @apply
  focus:outline-none focus:ring-2 focus:ring-purple-700 focus:ring-opacity-100
  focus:bg-white
  bg-gray-200
  w-80
  pl-3
  py-1
  rounded-l-md
  placeholder-opacity-100
}

.search-icon {
  @apply
  inline-flex items-center
  ml-0.5
  px-2
  bg-gray-100
  rounded-r-md
  text-gray-300

  /*hover:bg-gray-300
  hover:text-gray-500*/
  cursor-not-allowed
}

.right-side {
  @apply
  flex items-center
  justify-start
  space-x-3
  mr-2
}

.right-nav-link {
  @apply
  p-1
  rounded
  cursor-pointer
  flex justify-center items-center
  hover:bg-gray-200
}

.get-bits-link {
  @apply
  flex flex-row
  justify-center items-center
  bg-gray-200
  px-2 py-1
  rounded
  font-semibold
  text-sm
  cursor-pointer

  hover:bg-gray-300
}

.avatar {
  @apply
  inline-block
  relative
  h-8 w-8
}

.avatar-status {
  @apply
  absolute
  bg-white
  rounded-full
  right-0
  bottom-0.5
}

.avatar-status-offline {
  @apply
  w-1.5
  h-1.5
  bg-gray-400
  rounded-full
  m-0.5
}


</style>
