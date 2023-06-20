<!-- This example requires Tailwind CSS v2.0+ -->
<template>
  <div class="bg-amber-50">
    <div class="relative bg-indigo-600">
      <!-- Overlapping background -->
      <div aria-hidden="true" class="hidden absolute bg-amber-50 w-full h-6 bottom-0 lg:block" />

      <div class="relative max-w-2xl mx-auto pt-16 px-4 text-center sm:pt-32 sm:px-6 lg:max-w-7xl lg:px-8">
        <h1 class="text-4xl font-extrabold tracking-tight text-white sm:text-6xl">
          <span class="block lg:inline text-amber-200">Plans and Pricing</span>
          <!-- <span class="block lg:inline">no commitment.</span> -->
        </h1>
        <p class="mt-4 text-xl text-indigo-100">Flexible monthly plans to fit any workload.</p>
      </div>

      <h2 class="sr-only">Plans</h2>

      <!-- Toggle -->
      <div class="relative mt-12 flex justify-center sm:mt-16">
        <div class="bg-indigo-700 text-indigo-200 p-0.5 rounded-lg flex">
          <button @click="setPeriod" value="quaterly"
            class="ml-0.5 relative py-2 px-6 border border-transparent rounded-md text-sm font-medium  whitespace-nowrap hover:bg-indigo-800 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-indigo-700 focus:ring-amber-50 focus:z-10"
            :class="{'bg-amber-50 hover:!bg-indigo-50 text-indigo-700': period === 3}"
            >Quaterly</button>
          <button @click="setPeriod" value="biannually"
            class="ml-0.5 relative py-2 px-6 border border-transparent rounded-md text-sm font-medium  whitespace-nowrap hover:bg-indigo-800 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-indigo-700 focus:ring-amber-50 focus:z-10"
            :class="{'bg-amber-50 hover:!bg-indigo-50 text-indigo-700': period === 6}"
            >Biannually</button>
          <button @click="setPeriod" value="annually"
            class="ml-0.5 relative py-2 px-6 border border-transparent rounded-md text-sm font-medium whitespace-nowrap hover:bg-indigo-800 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-indigo-700 focus:ring-amber-50 focus:z-10"
            :class="{'bg-amber-50 hover:!bg-indigo-50 text-indigo-700': period === 12}"
            >Annually</button>
        </div>
      </div>

      <!-- Cards -->
      <div class="relative mt-8 max-w-2xl mx-auto px-4 pb-8 sm:mt-12 sm:px-6 lg:max-w-7xl lg:px-8 lg:pb-0">
        <!-- Decorative background -->
        <div aria-hidden="true"
          class="hidden absolute top-4 bottom-6 left-8 right-8 inset-0 bg-indigo-700 rounded-tl-lg rounded-tr-lg lg:block" />

        <div class="relative space-y-6 lg:space-y-0 lg:grid lg:grid-cols-3">
          <div v-for="plan in pricing.plans" :key="plan.title"
            :class="[plan.featured ? 'bg-amber-50 ring-2 ring-indigo-700 shadow-md' : 'bg-indigo-700 lg:bg-transparent', 'pt-6 px-6 pb-3 rounded-lg lg:px-8 lg:pt-12']">
            <div>
              <h3
                :class="[plan.featured ? 'text-indigo-600' : 'text-white', 'text-sm font-semibold uppercase tracking-wide']">
                {{ plan.title }}</h3>
              <div
                class="flex flex-col items-start sm:flex-row sm:items-center sm:justify-between lg:flex-col lg:items-start">
                <div class="mt-3 flex items-center">
                  <p
                    :class="[plan.featured ? 'text-indigo-600' : 'text-white', 'text-4xl font-extrabold tracking-tight']">
                    ${{ plan.priceMonthly }}</p>
                  <div class="ml-4">
                    <p :class="[plan.featured ? 'text-gray-700' : 'text-white', 'text-sm']">TTD / {{ period }} months</p>
                    <p :class="[plan.featured ? 'text-gray-500' : 'text-indigo-200', 'text-sm']">{{ (period / 3) * plan.hours }} hours of work</p>
                  </div>
                </div>
                <a href="#contact-form"
                  :class="[plan.featured ? 'bg-indigo-600 text-white hover:bg-indigo-700' : 'bg-amber-50 text-indigo-600 hover:bg-indigo-50', 'mt-6 w-full inline-block py-2 px-8 border border-transparent rounded-md shadow-sm text-center text-sm font-medium sm:mt-0 sm:w-auto lg:mt-6 lg:w-full']">Get started today</a>
              </div>
            </div>
            <h4 class="sr-only">Features</h4>
            <ul role="list"
              :class="[plan.featured ? 'border-gray-200 divide-amber-200' : 'border-indigo-500 divide-indigo-500 divide-opacity-75', 'mt-7 border-t divide-y lg:border-t-0']">
              <li v-for="mainFeature in plan.mainFeatures" :key="mainFeature.id" class="py-3 flex items-center">
                <CheckIcon :class="[plan.featured ? 'text-indigo-500' : 'text-indigo-200', 'w-5 h-5 flex-shrink-0']"
                  aria-hidden="true" />
                <span :class="[plan.featured ? 'text-gray-600' : 'text-white', 'ml-3 text-sm font-medium']">{{
                mainFeature.value }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>

    <!-- Feature comparison (up to lg) -->
    <section aria-labelledby="mobile-comparison-heading" class="lg:hidden">
      <h2 id="mobile-comparison-heading" class="sr-only">Feature comparison</h2>

      <div class="max-w-2xl mx-auto py-16 px-4 space-y-16 sm:px-6">
        <div v-for="(plan, mobilePlanIndex) in pricing.plans" :key="mobilePlanIndex" class="border-t border-amber-200">
          <div :class="[plan.featured ? 'border-indigo-600' : 'border-transparent', '-mt-px pt-6 border-t-2 sm:w-1/2']">
            <h3 :class="[plan.featured ? 'text-indigo-600' : 'text-gray-900', 'text-sm font-bold']">{{ plan.title }}
            </h3>
            <p class="mt-2 text-sm text-gray-500">{{ plan.description }}</p>
          </div>
          <h4 class="mt-10 text-sm font-bold text-gray-900">Catered for business</h4>

          <div class="mt-6 relative">
            <!-- Fake card background -->
            <div aria-hidden="true" class="hidden absolute inset-0 pointer-events-none sm:block">
              <div
                :class="[plan.featured ? 'shadow-md' : 'shadow', 'absolute right-0 w-1/2 h-full bg-white rounded-lg']" />
            </div>

            <div
              :class="[plan.featured ? 'ring-2 ring-indigo-600 shadow-md' : 'ring-1 ring-black ring-opacity-5 shadow', 'relative py-3 px-4 bg-white rounded-lg sm:p-0 sm:bg-transparent sm:rounded-none sm:ring-0 sm:shadow-none']">
              <dl class="divide-y divide-amber-200">
                <div v-for="feature in features" :key="feature.title"
                  class="py-3 flex items-center justify-between sm:grid sm:grid-cols-2">
                  <dt class="pr-4 text-sm font-medium text-gray-600">{{ feature.title }}</dt>
                  <dd class="flex items-center justify-end sm:px-4 sm:justify-center">
                    <span v-if="typeof feature.tiers[mobilePlanIndex].value === 'string'"
                      :class="[feature.tiers[mobilePlanIndex].featured ? 'text-indigo-600' : 'text-gray-900', 'text-sm font-medium']">{{
                      feature.tiers[mobilePlanIndex].value }}</span>
                    <template v-else>
                      <CheckIcon v-if="feature.tiers[mobilePlanIndex].value === true"
                        class="mx-auto h-5 w-5 text-indigo-600" aria-hidden="true" />
                      <XIcon v-else class="mx-auto h-5 w-5 text-gray-400" aria-hidden="true" />
                      <span class="sr-only">{{ feature.tiers[mobilePlanIndex].value === true ? 'Yes' : 'No' }}</span>
                    </template>
                  </dd>
                </div>
              </dl>
            </div>

            <!-- Fake card border -->
            <div aria-hidden="true" class="hidden absolute inset-0 pointer-events-none sm:block">
              <div
                :class="[plan.featured ? 'ring-2 ring-indigo-600' : 'ring-1 ring-black ring-opacity-5', 'absolute right-0 w-1/2 h-full rounded-lg']" />
            </div>
          </div>

          <h4 class="mt-10 text-sm font-bold text-gray-900">Other perks</h4>

          <div class="mt-6 relative">
            <!-- Fake card background -->
            <div aria-hidden="true" class="hidden absolute inset-0 pointer-events-none sm:block">
              <div
                :class="[plan.featured ? 'shadow-md' : 'shadow', 'absolute right-0 w-1/2 h-full bg-white rounded-lg']" />
            </div>

            <div
              :class="[plan.featured ? 'ring-2 ring-indigo-600 shadow-md' : 'ring-1 ring-black ring-opacity-5 shadow', 'relative py-3 px-4 bg-white rounded-lg sm:p-0 sm:bg-transparent sm:rounded-none sm:ring-0 sm:shadow-none']">
              <dl class="divide-y divide-amber-200">
                <div v-for="perk in perks" :key="perk.title" class="py-3 flex justify-between sm:grid sm:grid-cols-2">
                  <dt class="text-sm font-medium text-gray-600 sm:pr-4">{{ perk.title }}</dt>
                  <dd class="text-center sm:px-4">
                    <CheckIcon v-if="perk.tiers[mobilePlanIndex].value === true" class="mx-auto h-5 w-5 text-indigo-600"
                      aria-hidden="true" />
                    <XIcon v-else class="mx-auto h-5 w-5 text-gray-400" aria-hidden="true" />
                    <span class="sr-only">{{ perk.tiers[mobilePlanIndex].value === true ? 'Yes' : 'No' }}</span>
                  </dd>
                </div>
              </dl>
            </div>

            <!-- Fake card border -->
            <div aria-hidden="true" class="hidden absolute inset-0 pointer-events-none sm:block">
              <div
                :class="[plan.featured ? 'ring-2 ring-indigo-600' : 'ring-1 ring-black ring-opacity-5', 'absolute right-0 w-1/2 h-full rounded-lg']" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Feature comparison (lg+) -->
    <section aria-labelledby="comparison-heading" class="hidden lg:block">
      <h2 id="comparison-heading" class="sr-only">Feature comparison</h2>

      <div class="max-w-7xl mx-auto pb-32 py-24 px-8">
        <div class="w-full border-t border-amber-200 flex items-stretch">
          <div class="-mt-px w-1/4 py-6 pr-4 flex items-end">
            <h3 class="mt-auto text-sm font-bold text-gray-900">Catered for business</h3>
          </div>
          <div v-for="(plan, planIdx) in pricing.plans" :key="plan.title" aria-hidden="true"
            :class="[planIdx === pricing.plans.length - 1 ? '' : 'pr-4', '-mt-px pl-4 w-1/4']">
            <div :class="[plan.featured ? 'border-indigo-600' : 'border-transparent', 'py-6 border-t-2']">
              <p :class="[plan.featured ? 'text-indigo-600' : 'text-gray-900', 'text-sm font-bold']">{{ plan.title }}
              </p>
              <p class="mt-2 text-sm text-gray-500">{{ plan.description }}</p>
            </div>
          </div>
        </div>

        <div class="relative">
          <!-- Fake card backgrounds -->
          <div class="absolute inset-0 flex items-stretch pointer-events-none" aria-hidden="true">
            <div class="w-1/4 pr-4" />
            <div class="w-1/4 px-4">
              <div class="w-full h-full bg-white rounded-lg shadow" />
            </div>
            <div class="w-1/4 px-4">
              <div class="w-full h-full bg-white rounded-lg shadow-md" />
            </div>
            <div class="w-1/4 pl-4">
              <div class="w-full h-full bg-white rounded-lg shadow" />
            </div>
          </div>

          <table class="relative w-full">
            <caption class="sr-only">
              Business feature comparison
            </caption>
            <thead>
              <tr class="text-left">
                <th scope="col">
                  <span class="sr-only">Feature</span>
                </th>
                <th v-for="plan in pricing.plans" :key="plan.title" scope="col">
                  <span class="sr-only">{{ plan.title }} plan</span>
                </th>
              </tr>
            </thead>
            <tbody class="divide-y divide-amber-100">
              <tr v-for="feature in features" :key="feature.title">
                <th scope="row" class="w-1/4 py-3 pr-4 text-left text-sm font-medium text-gray-600">{{ feature.title }}
                </th>
                <td v-for="(tier, tierIdx) in feature.tiers" :key="tier.title"
                  :class="[tierIdx === feature.tiers.length - 1 ? 'pl-4' : 'px-4', 'relative w-1/4 py-0 text-center']">
                  <span class="relative w-full h-full py-3">
                    <span v-if="typeof tier.value === 'string'"
                      :class="[tier.featured ? 'text-indigo-600' : 'text-gray-900', 'text-sm font-medium']">{{
                      tier.value }}</span>
                    <template v-else>
                      <CheckIcon v-if="tier.value === true" class="mx-auto h-5 w-5 text-indigo-600"
                        aria-hidden="true" />
                      <XIcon v-else class="mx-auto h-5 w-5 text-gray-400" aria-hidden="true" />
                      <span class="sr-only">{{ tier.value === true ? 'Yes' : 'No' }}</span>
                    </template>
                  </span>
                </td>
              </tr>
            </tbody>
          </table>

          <!-- Fake card borders -->
          <div class="absolute inset-0 flex items-stretch pointer-events-none" aria-hidden="true">
            <div class="w-1/4 pr-4" />
            <div class="w-1/4 px-4">
              <div class="w-full h-full rounded-lg ring-1 ring-black ring-opacity-5" />
            </div>
            <div class="w-1/4 px-4">
              <div class="w-full h-full rounded-lg ring-2 ring-indigo-600 ring-opacity-100" />
            </div>
            <div class="w-1/4 pl-4">
              <div class="w-full h-full rounded-lg ring-1 ring-black ring-opacity-5" />
            </div>
          </div>
        </div>

        <h3 class="mt-10 text-sm font-bold text-gray-900">Other perks</h3>

        <div class="mt-6 relative">
          <!-- Fake card backgrounds -->
          <div class="absolute inset-0 flex items-stretch pointer-events-none" aria-hidden="true">
            <div class="w-1/4 pr-4" />
            <div class="w-1/4 px-4">
              <div class="w-full h-full bg-white rounded-lg shadow" />
            </div>
            <div class="w-1/4 px-4">
              <div class="w-full h-full bg-white rounded-lg shadow-md" />
            </div>
            <div class="w-1/4 pl-4">
              <div class="w-full h-full bg-white rounded-lg shadow" />
            </div>
          </div>

          <table class="relative w-full">
            <caption class="sr-only">
              Perk comparison
            </caption>
            <thead>
              <tr class="text-left">
                <th scope="col">
                  <span class="sr-only">Perk</span>
                </th>
                <th v-for="plan in pricing.plans" :key="plan.title" scope="col">
                  <span class="sr-only">{{ plan.title }} plan</span>
                </th>
              </tr>
            </thead>
            <tbody class="divide-y divide-amber-100">
              <tr v-for="perk in perks" :key="perk.title">
                <th scope="row" class="w-1/4 py-3 pr-4 text-left text-sm font-medium text-gray-600">{{ perk.title }}
                </th>
                <td v-for="(tier, tierIdx) in perk.tiers" :key="tier.title"
                  :class="[tierIdx === perk.tiers.length - 1 ? 'pl-4' : 'px-4', 'relative w-1/4 py-0 text-center']">
                  <span class="relative w-full h-full py-3">
                    <CheckIcon v-if="tier.value === true" class="mx-auto h-5 w-5 text-indigo-600" aria-hidden="true" />
                    <XIcon v-else class="mx-auto h-5 w-5 text-gray-400" aria-hidden="true" />
                    <span class="sr-only">{{ tier.value === true ? 'Yes' : 'No' }}</span>
                  </span>
                </td>
              </tr>
            </tbody>
          </table>

          <!-- Fake card borders -->
          <div class="absolute inset-0 flex items-stretch pointer-events-none" aria-hidden="true">
            <div class="w-1/4 pr-4" />
            <div class="w-1/4 px-4">
              <div class="w-full h-full rounded-lg ring-1 ring-black ring-opacity-5" />
            </div>
            <div class="w-1/4 px-4">
              <div class="w-full h-full rounded-lg ring-2 ring-indigo-600 ring-opacity-100" />
            </div>
            <div class="w-1/4 pl-4">
              <div class="w-full h-full rounded-lg ring-1 ring-black ring-opacity-5" />
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
import { CheckIcon, XIcon } from '@heroicons/vue/solid/index.js'
import { reactive, ref } from 'vue'

const period = ref(3);

const pricing = reactive({
  plans: [
    {
      title: 'Basic',
      featured: false,
      description: 'All your essential business finances, taken care of.',
      priceMonthly: 899,
      hours: 40,
      mainFeatures: [
        { id: 1, value: 'Customer Service' },
        { id: 2, value: 'Message & call response' },
        { id: 3, value: 'Social media content management' },
        { id: 4, value: 'Delivery & detail management' },
      ],
    },
    {
      title: 'Elite',
      featured: true,
      description: 'The best financial services for your thriving business.',
      priceMonthly: 1249,
      hours: 60,
      mainFeatures: [
        { id: 1, value: 'Customer Service' },
        { id: 2, value: 'Message & call response' },
        { id: 3, value: 'Social media & website content management' },
        { id: 4, value: 'Delivery & detail management' },
        { id: 6, value: 'Data entry & record keeping' },
        { id: 7, value: 'Market research' },
      ],
    },
    {
      title: 'Modern',
      featured: false,
      description: 'Convenient features to take your business to the next level.',
      priceMonthly: 1099,
      hours: 50,
      mainFeatures: [
        { id: 1, value: 'Customer Service' },
        { id: 2, value: 'Message & call response' },
        { id: 3, value: 'Social media & website content management' },
        { id: 4, value: 'Delivery & detail management' },
        { id: 6, value: 'Data entry & record keeping' },
      ],
    },
  ]
})

const features = [
  {
    title: 'Customer Service',
    tiers: [
      { title: 'basic', value: 'First point of contact' },
      { title: 'elite', featured: true, value: 'First point of contact' },
      { title: 'modern', value: 'First point of contact' },
    ],
  },
  {
    title: 'Social & Web Content Management',
    tiers: [
      { title: 'basic', value: '1 social media' },
      { title: 'elite', featured: true, value: '1 social media & 1 website or 2 social medias' },
      { title: 'modern', value: '2 social medias & 1 website' },
    ],
  },
  {
    title: 'Overviews As Assigned',
    tiers: [
      { title: 'basic', value: 'Weekly' },
      { title: 'elite', featured: true, value: 'Daily' },
      { title: 'modern', value: '2 weekly' },
    ],
  },
  {
    title: 'Availability',
    tiers: [
      { title: 'basic', value: '5 days a week' },
      { title: 'elite', featured: true, value: '7 days a week' },
      { title: 'modern', value: '6 days a week' },
    ],
  },
]
const perks = [
  {
    title: '24/7 customer support',
    tiers: [
      { title: 'starter', value: true },
      { title: 'popular', featured: true, value: true },
      { title: 'intermediate', value: true },
    ],
  },
  {
    title: 'Instant notifications',
    tiers: [
      { title: 'starter', value: true },
      { title: 'popular', featured: true, value: true },
      { title: 'intermediate', value: true },
    ],
  },
  {
    title: 'Budgeting tools',
    tiers: [
      { title: 'starter', value: true },
      { title: 'popular', featured: true, value: true },
      { title: 'intermediate', value: true },
    ],
  },
  {
    title: 'Digital receipts',
    tiers: [
      { title: 'starter', value: true },
      { title: 'popular', featured: true, value: true },
      { title: 'intermediate', value: true },
    ],
  },
]

function setPeriod(v) {
  if (v.target.value == 'quaterly') {
    period.value = 3;
    pricing.plans[0].priceMonthly = 899;
    pricing.plans[1].priceMonthly = 1249;
    pricing.plans[2].priceMonthly = 1099;
  }
  if (v.target.value == 'biannually') {
    period.value = 6;
    pricing.plans[0].priceMonthly = 1799;
    pricing.plans[1].priceMonthly = 2599;
    pricing.plans[2].priceMonthly = 2199;
  }
  if (v.target.value == 'annually') {
    period.value = 12;
    pricing.plans[0].priceMonthly = 3699;
    pricing.plans[1].priceMonthly = 5199;
    pricing.plans[2].priceMonthly = 4499;
  }
}
</script>