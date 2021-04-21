<template>
    <div class="" style="">
    <div class="bg-gray-100 h-screen" style="min-height: 660px;">
    
  
      <section @keydown.window.escape="open = false" x-init="$watch(&quot;open&quot;, o => !o &amp;&amp; window.setTimeout(() => (open = true), 1000))" v-if="open" class="fixed inset-0 overflow-hidden" aria-labelledby="slide-over-title" x-ref="dialog" role="dialog" aria-modal="true">
        <div class="absolute inset-0 overflow-hidden">
          <div x-description="Background overlay, show/hide based on slide-over state." class="absolute inset-0" @click="open = false" aria-hidden="true"></div>

          <div class="absolute inset-y-0 right-0 pl-10 max-w-full flex sm:pl-16">
          
              <transition enter-active-class="transform transition ease-in-out duration-500 sm:duration-700" enter-class="translate-x-full" enter-to-class="translate-x-0" leave-active-class="transform transition ease-in-out duration-500 sm:duration-700" leave-class="translate-x-0" leave-to-class="translate-x-full"><div v-if="open" class="w-screen max-w-2xl" x-description="Slide-over panel, show/hide based on slide-over state.">
                <div class="h-full flex flex-col bg-white shadow-xl overflow-y-scroll">
                  <div class="px-4 py-6 sm:px-6">
                    <div class="flex items-start justify-between">
                      <h2 class="text-lg font-medium text-gray-900" id="slide-over-title">
                        Profile
                      </h2>
                      <div class="ml-3 h-7 flex items-center">
                        <button class="bg-white rounded-md text-gray-400 hover:text-gray-500 focus:ring-2 focus:ring-indigo-500" @click="open = false">
                          <span class="sr-only">Close panel</span>
                          <svg class="h-6 w-6" x-description="Heroicon name: outline/x" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
  </svg>
                        </button>
                      </div>
                    </div>
                  </div>
                  <!-- Main -->
                  <div class="divide-y divide-gray-200">
                    <div class="pb-6">
                      <div class="bg-indigo-700 h-24 sm:h-20 lg:h-28"></div>
                      <div class="-mt-12 flow-root px-4 sm:-mt-8 sm:flex sm:items-end sm:px-6 lg:-mt-15">
                        <div>
                          <div class="-m-1 flex">
                            <div class="inline-flex rounded-lg overflow-hidden border-4 border-white">
                              <img class="flex-shrink-0 h-24 w-24 sm:h-40 sm:w-40 lg:w-48 lg:h-48" src="https://images.unsplash.com/photo-1501031170107-cfd33f0cbdcc?ixlib=rb-1.2.1&amp;ixqx=cII20c177f&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=crop&amp;w=256&amp;h=256&amp;q=80" alt="">
                            </div>
                          </div>
                        </div>
                        <div class="mt-6 sm:ml-6 sm:flex-1">
                          <div>
                            <div class="flex items-center">
                              <h3 class="font-bold text-xl text-gray-900 sm:text-2xl">Ashley Porter</h3>
                              <span class="ml-2.5 bg-green-400 flex-shrink-0 inline-block h-2 w-2 rounded-full">
                                <span class="sr-only">Online</span>
                              </span>
                            </div>
                            <p class="text-sm text-gray-500">@ashleyporter</p>
                          </div>
                          <div class="mt-5 flex flex-wrap space-y-3 sm:space-y-0 sm:space-x-3">
                            <button type="button" class="flex-shrink-0 w-full inline-flex items-center justify-center px-4 py-2 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 sm:flex-1">
                              Message
                            </button>
                            <button type="button" class="flex-1 w-full inline-flex items-center justify-center px-4 py-2 border border-gray-300 rounded-md shadow-sm text-sm font-medium text-gray-700 bg-white hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                              Call
                            </button>
                            <span class="ml-3 inline-flex sm:ml-0">
                              <div @keydown.escape.stop="open = false" @click.away="open = false" class="relative inline-block text-left">
                                <button type="button" class="inline-flex items-center p-2 border border-gray-300 rounded-md shadow-sm text-sm font-medium text-gray-400 bg-white hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500" id="options-menu" aria-expanded="false" @click="open = !open" aria-haspopup="true" x-bind:aria-expanded="open">
                                  <span class="sr-only">Open options menu</span>
                                  <svg class="h-5 w-5" x-description="Heroicon name: solid/dots-vertical" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
    <path d="M10 6a2 2 0 110-4 2 2 0 010 4zM10 12a2 2 0 110-4 2 2 0 010 4zM10 18a2 2 0 110-4 2 2 0 010 4z"></path>
  </svg>
                                </button>
                              
                                  <transition enter-active-class="transition ease-out duration-100" enter-class="transform opacity-0 scale-95" enter-to-class="transform opacity-100 scale-100" leave-active-class="transition ease-in duration-75" leave-class="transform opacity-100 scale-100" leave-to-class="transform opacity-0 scale-95"><div v-if="open" x-description="Dropdown panel, show/hide based on dropdown state." class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none" role="menu" aria-orientation="vertical" aria-labelledby="options-menu">
                                    <div class="py-1" role="none">
                                      <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">View profile</a>
                                      <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 hover:text-gray-900" role="menuitem">Copy profile link</a>
                                    </div>
                                  </div></transition>
                              
                              </div>
                            </span>
                          </div>
                        </div>
                      </div>
                    </div>
                    <div class="px-4 py-5 sm:px-0 sm:py-0">
                      <dl class="space-y-8 sm:divide-y sm:divide-gray-200 sm:space-y-0">
                        <div class="sm:flex sm:px-6 sm:py-5">
                          <dt class="text-sm font-medium text-gray-500 sm:w-40 sm:flex-shrink-0 lg:w-48">
                            Bio
                          </dt>
                          <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:ml-6 sm:col-span-2">
                            <p>
                              Enim feugiat ut ipsum, neque ut. Tristique mi id elementum praesent. Gravida in tempus feugiat netus enim aliquet a, quam scelerisque. Dictumst in convallis nec in bibendum aenean arcu.
                            </p>
                          </dd>
                        </div>
                        <div class="sm:flex sm:px-6 sm:py-5">
                          <dt class="text-sm font-medium text-gray-500 sm:w-40 sm:flex-shrink-0 lg:w-48">
                            Location
                          </dt>
                          <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:ml-6 sm:col-span-2">
                            New York, NY, USA
                          </dd>
                        </div>
                        <div class="sm:flex sm:px-6 sm:py-5">
                          <dt class="text-sm font-medium text-gray-500 sm:w-40 sm:flex-shrink-0 lg:w-48">
                            Website
                          </dt>
                          <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:ml-6 sm:col-span-2">
                            ashleyporter.com
                          </dd>
                        </div>
                        <div class="sm:flex sm:px-6 sm:py-5">
                          <dt class="text-sm font-medium text-gray-500 sm:w-40 sm:flex-shrink-0 lg:w-48">
                            Birthday
                          </dt>
                          <dd class="mt-1 text-sm text-gray-900 sm:mt-0 sm:ml-6 sm:col-span-2">
                            <time datetime="1982-06-23">
                              June 23, 1982
                            </time>
                          </dd>
                        </div>
                      </dl>
                    </div>
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
    open: false,
  })
}
</script>
