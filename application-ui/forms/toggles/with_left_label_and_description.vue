<template>
    <div class="" style="">
    <div class="p-8 flex items-center justify-center bg-white">
      <div class="max-w-xl w-full -mx-auto">
      
    <div class="flex items-center justify-between">
      <span class="flex-grow flex flex-col" id="availability-label" @click="on = !on; $refs.switch.focus()">
        <span class="text-sm font-medium text-gray-900">Available to hire</span>
        <span class="text-sm text-gray-500">Nulla amet tempus sit accumsan. Aliquet turpis sed sit lacinia.</span>
      </span>
      <button type="button" class="bg-gray-200 relative inline-flex flex-shrink-0 h-6 w-11 border-2 border-transparent rounded-full cursor-pointer transition-colors ease-in-out duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500" aria-pressed="false" x-ref="switch" x-state:on="Enabled" x-state:off="Not Enabled" :class="{ 'bg-indigo-600': on, 'bg-gray-200': !(on) }" aria-labelledby="availability-label" :aria-pressed="on.toString()" @click="on = !on">
        <span class="sr-only">Use setting</span>
        <span aria-hidden="true" class="translate-x-0 pointer-events-none inline-block h-5 w-5 rounded-full bg-white shadow transform ring-0 transition ease-in-out duration-200" x-state:on="Enabled" x-state:off="Not Enabled" :class="{ 'translate-x-5': on, 'translate-x-0': !(on) }"></span>
      </button>
    </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
	on: false,
  })
}
</script>
