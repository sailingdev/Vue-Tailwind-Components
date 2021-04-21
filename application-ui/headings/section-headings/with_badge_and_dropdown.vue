<template>
    <div class="" style="">
    <div class="bg-white">
      <div class="px-4 py-12 max-w-7xl mx-auto sm:px-6 lg:px-8">
      
    <div class="pb-5 border-b border-gray-200">
      <div class="sm:flex sm:justify-between sm:items-baseline">
        <div class="sm:w-0 sm:flex-1">
          <h1 id="message-heading" class="text-lg font-medium text-gray-900">
            Full-Stack Developer
          </h1>
          <p class="mt-1 text-sm text-gray-500 overflow-hidden overflow-ellipsis">
            Checkout and Payments Team
          </p>
        </div>

        <div class="mt-4 flex items-center justify-between sm:mt-0 sm:ml-6 sm:flex-shrink-0 sm:justify-start">
          <span class="inline-flex items-center px-3 py-0.5 rounded-full text-sm font-medium bg-green-100 text-green-800">
            Open
          </span>
          <div @keydown.escape.stop="open = false" @click.away="open = false" class="ml-3 relative inline-block text-left">
            <div>
              <button type="button" class="-my-2 p-2 rounded-full bg-white flex items-center text-gray-400 hover:text-gray-600 focus:outline-none focus:ring-2 focus:ring-indigo-500" id="menu-1" aria-expanded="false" @click="open = !open" aria-haspopup="true" x-bind:aria-expanded="open">
                <span class="sr-only">Open options</span>
                <svg class="h-5 w-5" x-description="Heroicon name: solid/dots-vertical" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
    <path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path>
  </svg>
              </button>
            </div>

          
              <transition enter-active-class="transition ease-out duration-100" enter-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95"><div v-if="open" x-description="Dropdown menu, show/hide based on menu state." class="origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="menu-1">
                <div class="py-1" role="none">
                  <a href="#" class="flex justify-between px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">
                      <span>Edit</span>
                    </a>
                  <a href="#" class="flex justify-between px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">
                      <span>Duplicate</span>
                    </a>
                  <button type="button" class="w-full flex justify-between px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">
                      <span>Archive</span>
                    </button>
                </div>
              </div></transition>
          
          </div>
        </div>
      </div>
    </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
	open: false,
  })
}
</script>
