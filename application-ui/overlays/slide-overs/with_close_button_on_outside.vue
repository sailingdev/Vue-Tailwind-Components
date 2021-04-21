<template>
    <div class="" style="">
    <div class="bg-gray-100 h-screen" style="min-height: 500px;">
    
  
      <section @keydown.window.escape="open = false" x-init="$watch(&quot;open&quot;, o => !o &amp;&amp; window.setTimeout(() => (open = true), 1000))" v-if="open" class="fixed inset-0 overflow-hidden" aria-labelledby="slide-over-title" x-ref="dialog" role="dialog" aria-modal="true">
        <div class="absolute inset-0 overflow-hidden">
        
            <transition enter-active-class="ease-in-out duration-500" enter-class="opacity-0" enter-to-class="opacity-100" leave-active-class="ease-in-out duration-500" leave-class="opacity-100" leave-to-class="opacity-0"><div v-if="open" x-description="Background overlay, show/hide based on slide-over state." class="absolute inset-0 bg-gray-500 bg-opacity-75 transition-opacity" @click="open = false" aria-hidden="true"></div></transition>
        
          <div class="absolute inset-y-0 right-0 pl-10 max-w-full flex">
          
              <transition enter-active-class="transform transition ease-in-out duration-500 sm:duration-700" enter-class="translate-x-full" enter-to-class="translate-x-0" leave-active-class="transform transition ease-in-out duration-500 sm:duration-700" leave-class="translate-x-0" leave-to-class="translate-x-full"><div v-if="open" class="relative w-screen max-w-md" x-description="Slide-over panel, show/hide based on slide-over state.">
              
                  <transition enter-active-class="ease-in-out duration-500" enter-class="opacity-0" enter-to-class="opacity-100" leave-active-class="ease-in-out duration-500" leave-class="opacity-100" leave-to-class="opacity-0"><div v-if="open" x-description="Close button, show/hide based on slide-over state." class="absolute top-0 left-0 -ml-8 pt-4 pr-2 flex sm:-ml-10 sm:pr-4">
                    <button class="rounded-md text-gray-300 hover:text-white focus:outline-none focus:ring-2 focus:ring-white" @click="open = false">
                      <span class="sr-only">Close panel</span>
                      <svg class="h-6 w-6" x-description="Heroicon name: outline/x" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
  </svg>
                    </button>
                  </div></transition>
              
                <div class="h-full flex flex-col py-6 bg-white shadow-xl overflow-y-scroll">
                  <div class="px-4 sm:px-6">
                    <h2 class="text-lg font-medium text-gray-900" id="slide-over-title">
                      Panel title
                    </h2>
                  </div>
                  <div class="mt-6 relative flex-1 px-4 sm:px-6">
                    <!-- Replace with your content -->
                    <div class="absolute inset-0 px-4 sm:px-6">
                      <div class="h-full border-2 border-dashed border-gray-200" aria-hidden="true"></div>
                    </div>
                    <!-- /End replace -->
                  </div>
                </div>
              </div></transition>
          
          </div>
        </div>
      </section>
  

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
