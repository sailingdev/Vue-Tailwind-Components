<template>
    <div class="" style="">
    <div class="p-8 bg-white flex items-start justify-center" style="min-height: 256px;">
    
    <span class="relative z-0 inline-flex shadow-sm rounded-md">
      <button type="button" class="relative inline-flex items-center px-4 py-2 rounded-l-md border border-gray-300 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-1 focus:ring-indigo-500 focus:border-indigo-500">
        Save changes
      </button>
      <span @keydown.escape.stop="open = false" @click.away="open = false" class="-ml-px relative block">
        <button type="button" class="relative inline-flex items-center px-2 py-2 rounded-r-md border border-gray-300 bg-white text-sm font-medium text-gray-500 hover:bg-gray-50 focus:z-10 focus:outline-none focus:ring-1 focus:ring-indigo-500 focus:border-indigo-500" id="option-menu" aria-expanded="true" @click="open = !open" aria-haspopup="true" x-bind:aria-expanded="open">
          <span class="sr-only">Open options</span>
          <svg class="h-5 w-5" x-description="Heroicon name: solid/chevron-down" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
    <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"></path>
  </svg>
        </button>
      
          <transition enter-active-class="transition ease-out duration-100" enter-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95"><div x-description="Dropdown menu, show/hide based on menu state." v-if="open" class="origin-top-right absolute right-0 mt-2 -mr-1 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="option-menu">
            <div class="py-1" role="none">
            
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">
                    Save and schedule
                  </a>
            
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">
                    Save and publish
                  </a>
            
                <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">
                    Export PDF
                  </a>
            
            </div>
          </div></transition>
      
      </span>
    </span>

    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
	open: true,
  })
}
</script>
