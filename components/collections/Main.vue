<template>
  <div>
    <Disclosure
      as="nav"
      class="fixed top-0 left-0 w-full bg-white shadow z-50"
      v-slot="{ open }"
    >
      <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
        <div class="flex h-16 justify-between">
          <div class="flex">
            <div class="-ml-2 mr-2 flex items-center md:hidden">
              <!-- Mobile menu button -->
              <DisclosureButton
                class="inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500"
              >
                <span class="sr-only">Open main menu</span>
                <Bars3Icon
                  v-if="!open"
                  class="block h-6 w-6"
                  aria-hidden="true"
                />
                <XMarkIcon v-else class="block h-6 w-6" aria-hidden="true" />
              </DisclosureButton>
            </div>
            <div class="flex flex-shrink-0 items-center">
              <img
                class="block h-8 w-auto lg:hidden"
                src=" https://ninjachat.com/images/logo.svg?v=1680096338629045558"
              />
              <img
                class="hidden h-8 w-auto lg:block"
                src=" https://ninjachat.com/images/logo.svg?v=1680096338629045558"
              />
            </div>
          </div>
          <ChevronDownIcon class="h-5 w-5" aria-hidden="true" />
          <div class="flex items-center">
            <div class="flex-shrink-0">
              <div class="hidden md:ml-6 md:flex md:space-x-8">
                <a
                  href="#"
                  class="inline-flex items-center border-b-2 border-indigo-500 px-1 pt-1 text-sm font-medium text-gray-900"
                  >Features</a
                >
                <a
                  href="#"
                  class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
                  >Pricing</a
                >
                <a
                  href="#"
                  class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
                  >Resources</a
                >
                <a
                  href="#"
                  class="inline-flex items-center border-b-2 border-transparent px-1 pt-1 text-sm font-medium text-gray-500 hover:border-gray-300 hover:text-gray-700"
                  >Login</a
                >
              </div>
            </div>
            <div
              class="hidden md:ml-4 md:flex md:flex-shrink-0 md:items-center"
            >
              <button
                type="button"
                class="relative inline-flex items-center gap-x-1.5 rounded-md bg-indigo-600 px-3 py-2 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
              >
                Sign Up
              </button>
            </div>
          </div>
        </div>
      </div>
    </Disclosure>
    <collectionsPage1 />
    <collectionsPage2 />
    <collectionsPage3 />
    <collectionsPage4 />
    <CollectionsPage5/>
    <CollectionsPage6/>
  </div>
</template>
<script setup>
import {
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  Menu,
  MenuButton,
  MenuItem,
  MenuItems,
} from "@headlessui/vue";
import { Bars3Icon, BellIcon, XMarkIcon } from "@heroicons/vue/24/outline";
import { PlusIcon } from "@heroicons/vue/20/solid";
</script>
