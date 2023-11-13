<template>
  <div class="flex justify-center">
    <div class="fixed top-16 w-56 max-[230px]:w-full text-right">
      <UDropdown
        :items="items"
        :ui="{
          item: {
            base: 'group flex items-center gap-2 w-full',
            rounded: 'rounded-md',
            padding: 'px-2 py-2',
            size: 'text-sm',
            active:
              'bg-violet-500 dark:bg-violet-950 text-white dark:text-gray-200 ', //
            disabled: 'cursor-not-allowed opacity-50',
            shortcuts: 'hidden md:inline-flex flex-shrink-0 gap-0.5 ms-auto',
          },
          width: 'w-56 max-[230px]:w-[100vw]',
          ring: 'ring-1 ring-gray-100 dark:ring-gray-700',
        }"
        :popper="{ placement: 'bottom-end' }"
      >
        <UButton
          :class="[
            'inline-flex w-full justify-center rounded-md bg-black/20 px-4 py-2 text-sm font-medium text-white hover:bg-black/30 focus:outline-none focus-visible:ring-2 focus-visible:ring-white/75',
            'dark:bg-violet-400  hover:dark:bg-violet-500 focus-visible:ring-white/75 text-white',
          ]"
          label="Options"
        />
      </UDropdown>
    </div>
  </div>
</template>

<script setup>
const items = [
  [
    {
      label: "Account",
    },
    {
      label: "Edit",
    },
  ],
  [
    {
      label: "Make a copy",
    },
    {
      label: "Archive",
    },
  ],
  [
    {
      label: "Delete",
    },
  ],
];
</script>
