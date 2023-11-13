<template>
  <div class="fixed top-16 w-56 max-[230px]:w-full text-center">
    <UDropdown
      :items="items"
      :ui="{
        item: {
          padding: 'px-2 py-2',
          active:
            'bg-violet-500 dark:bg-violet-950 text-white dark:text-gray-200 ', //
          disabled: 'cursor-not-allowed opacity-50',
          icon: {
            base: 'flex-shrink-0 h-4 w-4 ',
            active: 'text-white dark:text-gray-200',
            inactive: 'text-gray-400 dark:bg-gray-400',
          },
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
</template>

<script setup>
const items = [
  [
    {
      label: "Account",
      icon: "i-heroicons-user-20-solid",
    },
    {
      label: "Edit",
      icon: "i-heroicons-pencil-square-20-solid",
    },
  ],
  [
    {
      label: "Make a copy",
      icon: "i-heroicons-document-duplicate-20-solid",
    },
    {
      label: "Archive",
      icon: "i-heroicons-archive-box-20-solid",
    },
  ],
  [
    {
      label: "Delete",
      icon: "i-heroicons-trash-20-solid",
    },
  ],
];
</script>
