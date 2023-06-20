<!-- This example requires Tailwind CSS v2.0+ -->
<template>
    <div class="bg-amber-50 overflow-hidden">
      <div class="relative max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
        <svg class="absolute top-0 left-full transform -translate-x-1/2 -translate-y-3/4 lg:left-auto lg:right-full lg:translate-x-2/3 lg:translate-y-1/4" width="404" height="784" fill="none" viewBox="0 0 404 784" aria-hidden="true">
          <defs>
            <pattern id="8b1b5f72-e944-4457-af67-0c6d15a99f38" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-amber-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="784" fill="url(#8b1b5f72-e944-4457-af67-0c6d15a99f38)" />
        </svg>
  
        <div class="relative lg:grid lg:grid-cols-3 lg:gap-x-8">
          <div class="lg:col-span-1">
            <h2 class="text-3xl font-extrabold tracking-tight text-gray-900 sm:text-4xl">Supercharge your life with a Virtual Assistant</h2>
          </div>
          <dl class="mt-10 space-y-10 sm:space-y-0 sm:grid sm:grid-cols-2 sm:gap-x-8 sm:gap-y-10 lg:mt-0 lg:col-span-2">
            <div v-for="feature in features" :key="feature.name">
              <dt>
                <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                  <component :is="feature.icon" class="h-6 w-6" aria-hidden="true" />
                </div>
                <p class="mt-5 text-lg leading-6 font-medium text-gray-900">{{ feature.name }}</p>
              </dt>
              <dd class="mt-2 text-base text-gray-500">
                {{ feature.description }}
              </dd>
            </div>
          </dl>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { SearchIcon, CalendarIcon, ThumbUpIcon, CalculatorIcon } from '@heroicons/vue/outline/index.js'
  
  const features = [
    {
      name: 'Research and Reports',
      description: 'Need help with your research or reports. Our virtual assistants can help you with everything from data entry to finding information online.',
      icon: SearchIcon,
    },
    {
      name: 'Expenses and Invoicing',
      description:
        'Streamline your expenses and invoicing. Our virtual assistants can help keep track of spending, prepare invoices, and even file your taxes.',
      icon: CalculatorIcon,
    },
    {
      name: 'Scheduling and Planning',
      description:
        'Looking for help with scheduling and planning. Our virtual assistants can help keep track of your schedule, plan ahead for upcoming appointments and deadlines, and make sure you\'re staying on track.',
      icon: CalendarIcon,
    },
    {
      name: 'Marketing and Social Media',
      description:
        'We\'ll take care of your marketing and social media needs. Our virtual assistants are experts crafting effective marketing materials. Save time and money and let us take care of the details.',
      icon: ThumbUpIcon,
    },
  ]
  </script>