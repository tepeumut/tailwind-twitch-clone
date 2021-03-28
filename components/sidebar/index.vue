<template>
  <div class="section">
    <div class="sidebar-content">
      <div class="sidebar-channels">
        <div class="sidebar-channels-header">
          <div class="sidebar-channels-title">
            FOLLOWED CHANNELS
          </div>
          <div class="sidebar-collapse">
            <svg class="h-5 w-5" viewBox="0 0 20 20" x="0px" y="0px">
              <g>
                <path d="M16 16V4h2v12h-2zM6 9l2.501-2.5-1.5-1.5-5 5 5 5 1.5-1.5-2.5-2.5h8V9H6z"></path>
              </g>
            </svg>
          </div>
        </div>
        <div class="following-channels-list">
          <SidebarChannel v-for="i in 10" :key="i" :is-online="true"/>
          <SidebarChannel :is-online="false"/>
        </div>
      </div>
      <div class="sidebar-channels mt-2">
        <div class="sidebar-channels-header">
          <div class="sidebar-channels-title">
            RECOMMENDED CHANNELS
          </div>
        </div>
        <div class="following-channels-list">
          <SidebarChannel v-for="i in 6" :key="i" :is-online="true"/>
          <SidebarChannel :is-online="false"/>
        </div>
      </div>
    </div>
    <div class="sidebar-footer">
      <div class="search-friend">
      <span class="search-icon">
        <svg class="w-5 h-5" viewBox="0 0 20 20" x="0px" y="0px"><g><path fill-rule="evenodd" d="M13.192 14.606a7 7 0 111.414-1.414l3.101 3.1-1.414 1.415-3.1-3.1zM14 9A5 5 0 114 9a5 5 0 0110 0z" clip-rule="evenodd" fill="currentColor"></path></g></svg>
      </span>
        <input type="text"
               placeholder="Search to Add Friends"
               class="search-input"/>
      </div>
    </div>
  </div>
</template>

<script>
import SidebarChannel from "@/components/sidebarChannel";

export default {
  name: "sidebar",
  components: {SidebarChannel}
}
</script>

<style scoped>
.section {
  @apply
  h-full
  flex flex-col
  bg-gray-100
  w-60
}

.sidebar-content {
  @apply
    max-h-screen
  overflow-x-hidden
  overflow-y-auto
}

.sidebar-channels-header {
  @apply
  flex justify-between items-center
  px-3 pt-3 pb-1
}

.sidebar-channels-title {
  @apply
  text-sm
  font-semibold
}

.sidebar-collapse {
  @apply
  rounded-md
  p-1
  hover:bg-gray-300
}

.sidebar-footer {
  @apply
  bg-gray-200
}

.search-friend {
  @apply
  relative
  p-4
  border-t border-gray-300
}

.search-input {
  @apply
  text-sm
  text-gray-700
  focus:outline-none focus:ring-2 focus:ring-purple-700 focus:ring-opacity-100
  focus:bg-white
  bg-gray-300
  w-full
  pl-7
  py-1
  rounded
}

.search-icon {
  @apply
  absolute
  top-5
  left-5
  text-gray-600
}

</style>
