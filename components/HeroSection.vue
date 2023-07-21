<!-- This example requires Tailwind CSS v2.0+ -->
<template>
    <div class="relative bg-amber-50 overflow-hidden">
      <div class="hidden sm:block sm:absolute sm:inset-y-0 sm:h-full sm:w-full" aria-hidden="true">
        <div class="relative h-full max-w-7xl mx-auto">
          <svg class="absolute right-full transform translate-y-1/4 translate-x-1/4 lg:translate-x-1/2" width="404" height="784" fill="none" viewBox="0 0 404 784">
            <defs>
              <pattern id="f210dbf6-a58d-4871-961e-36d5016a0f49" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                <rect x="0" y="0" width="4" height="4" class="text-amber-200" fill="currentColor" />
              </pattern>
            </defs>
            <rect width="404" height="784" fill="url(#f210dbf6-a58d-4871-961e-36d5016a0f49)" />
          </svg>
          <svg class="absolute left-full transform -translate-y-3/4 -translate-x-1/4 md:-translate-y-1/2 lg:-translate-x-1/2" width="404" height="784" fill="none" viewBox="0 0 404 784">
            <defs>
              <pattern id="5d0dd344-b041-4d26-bec4-8d33ea57ec9b" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                <rect x="0" y="0" width="4" height="4" class="text-amber-200" fill="currentColor" />
              </pattern>
            </defs>
            <rect width="404" height="784" fill="url(#5d0dd344-b041-4d26-bec4-8d33ea57ec9b)" />
          </svg>
        </div>
      </div>
  
      <div class="relative pt-6 pb-16 sm:pb-24">
        <Popover>
          <div class="max-w-7xl mx-auto px-4 sm:px-6">
            <nav class="relative flex items-center justify-between sm:h-10 md:justify-center" aria-label="Global">
              <div class="flex items-center flex-1 md:absolute md:inset-y-0 md:left-0">
                <div class="flex items-center justify-between w-full md:w-auto">
                  <a href="/">
                    <span class="sr-only">Assist U</span>
                    <img class="h-10 w-auto sm:h-12" :src="Logo" alt="AssistU" />
                  </a>
                </div>
              </div>
              <div class="md:absolute md:flex md:items-center md:justify-end md:inset-y-0 md:right-0">
                <!-- <span class="inline-flex rounded-md shadow">
                  <a href="https://assistyou.online/worksuite/login" class="inline-flex items-center px-4 py-2 border border-transparent text-base font-medium rounded-md text-indigo-600 bg-white hover:bg-gray-50"> Log in </a>
                </span> -->
              </div>
            </nav>
          </div>
        </Popover>
  
        <main class="mt-16 mx-auto max-w-7xl px-4 sm:mt-24">
          <div class="text-center">
            <h1 class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl">
              <span class="block xl:inline">Thinking about getting a</span>
              {{ ' ' }}
              <span class="block text-indigo-600 xl:inline">virtual assistant?</span>
            </h1>
            <p class="mt-3 max-w-md mx-auto text-base text-gray-500 sm:text-lg md:mt-5 md:text-xl md:max-w-3xl">Let us prove how much time and money a virtual assistant can save you.</p>
            <div class="mt-5 max-w-md mx-auto sm:flex sm:justify-center md:mt-8">
              <div class="rounded-md shadow">
                <a href="#contact-form" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-bold rounded-md text-amber-100 bg-indigo-600 hover:bg-indigo-700 md:py-4 md:text-lg md:px-10"> Contact Us Today </a>
              </div>
              <!-- <div class="mt-3 rounded-md shadow sm:mt-0 sm:ml-3">
                <a href="#" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-indigo-600 bg-white hover:bg-gray-50 md:py-4 md:text-lg md:px-10"> Live demo </a>
              </div> -->
            </div>
          </div>
        </main>
      </div>
    </div>
  </template>
  
  <script setup>
  import Logo from '@/assets/img/logo.png'
  import { Popover } from '@headlessui/vue'

  </script>