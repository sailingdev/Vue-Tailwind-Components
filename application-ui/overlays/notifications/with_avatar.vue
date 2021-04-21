<template>
    <div class="" style="">
    <div class="bg-gray-100" style="min-height: 320px;">
    
  
      <div v-if="show" class="fixed inset-0 flex items-end justify-center px-4 py-6 pointer-events-none sm:p-6 sm:items-start sm:justify-end">
      
          <transition enter-active-class="transform ease-out duration-300 transition" enter-class="translate-y-2 opacity-0 sm:translate-y-0 sm:translate-x-2" enter-to-class="translate-y-0 opacity-100 sm:translate-x-0" leave-active-class="transition ease-in duration-100" leave-class="opacity-100" leave-to-class="opacity-0"><div v-if="show" x-description="Notification panel, show/hide based on alert state." class="max-w-md w-full bg-white shadow-lg rounded-lg pointer-events-auto flex ring-1 ring-black ring-opacity-5">
            <div class="w-0 flex-1 p-4">
              <div class="flex items-start">
                <div class="flex-shrink-0 pt-0.5">
                  <img class="h-10 w-10 rounded-full" src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&amp;ixqx=cII20c177f&amp;ixid=eyJhcHBfaWQiOjEyMDd9&amp;auto=format&amp;fit=facearea&amp;facepad=2.2&amp;w=160&amp;h=160&amp;q=80" alt="">
                </div>
                <div class="ml-3 w-0 flex-1">
                  <p class="text-sm font-medium text-gray-900">
                    Emilia Gates
                  </p>
                  <p class="mt-1 text-sm text-gray-500">
                    Sure! 8:30pm works great!
                  </p>
                </div>
              </div>
            </div>
            <div class="flex border-l border-gray-200">
              <button @click="show = false; setTimeout(() => show = true, 1000)" class="w-full border border-transparent rounded-none rounded-r-lg p-4 flex items-center justify-center text-sm font-medium text-indigo-600 hover:text-indigo-500 focus:outline-none focus:ring-2 focus:ring-indigo-500">
                Reply
              </button>
            </div>
          </div></transition>
      
      </div>
  

    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
	show: true,
  })
}
</script>
