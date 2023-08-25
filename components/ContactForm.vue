<template>
  <div id="contact-form" class="bg-amber-50 py-20">
    <!-- Header -->
      <div class="py-16 lg:py-28">
        <div class="relative z-10 mx-auto max-w-7xl pl-4 pr-8 sm:px-6 lg:px-8">
          <h1 class="text-4xl font-bold tracking-tight text-warm-gray-900 sm:text-5xl lg:text-6xl">Get in touch</h1>
          <p class="mt-6 max-w-3xl text-xl text-gray-600">We offer a variety of services to help you with your business
          needs.</p>
        </div>
      </div>

    <!-- Contact section -->
    <section class="relative" aria-labelledby="contact-heading">
      <div class="absolute h-1/2 w-full bg-amber-50" aria-hidden="true" />
      <!-- Decorative dot pattern -->
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="relative bg-white shadow-xl">
          <h2 id="contact-heading" class="sr-only">Contact us</h2>

          <div class="grid grid-cols-1 lg:grid-cols-3">
            <!-- Contact information -->
            <div class="relative overflow-hidden bg-gradient-to-b from-indigo-500 to-indigo-600 py-10 px-6 sm:px-10 xl:p-12">
              <!-- Decorative angle backgrounds -->
              <div class="pointer-events-none absolute inset-0 sm:hidden" aria-hidden="true">
                <svg class="absolute inset-0 h-full w-full" width="343" height="388" viewBox="0 0 343 388" fill="none"
                  preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
                  <path d="M-99 461.107L608.107-246l707.103 707.107-707.103 707.103L-99 461.107z" fill="url(#linear1)"
                    fill-opacity=".1" />
                  <defs>
                    <linearGradient id="linear1" x1="254.553" y1="107.554" x2="961.66" y2="814.66"
                      gradientUnits="userSpaceOnUse">
                      <stop stop-color="#fff" />
                      <stop offset="1" stop-color="#fff" stop-opacity="0" />
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <div class="pointer-events-none absolute top-0 right-0 bottom-0 hidden w-1/2 sm:block lg:hidden"
                aria-hidden="true">
                <svg class="absolute inset-0 h-full w-full" width="359" height="339" viewBox="0 0 359 339" fill="none"
                  preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
                  <path d="M-161 382.107L546.107-325l707.103 707.107-707.103 707.103L-161 382.107z" fill="url(#linear2)"
                    fill-opacity=".1" />
                  <defs>
                    <linearGradient id="linear2" x1="192.553" y1="28.553" x2="899.66" y2="735.66"
                      gradientUnits="userSpaceOnUse">
                      <stop stop-color="#fff" />
                      <stop offset="1" stop-color="#fff" stop-opacity="0" />
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <div class="pointer-events-none absolute top-0 right-0 bottom-0 hidden w-1/2 lg:block" aria-hidden="true">
                <svg class="absolute inset-0 h-full w-full" width="160" height="678" viewBox="0 0 160 678" fill="none"
                  preserveAspectRatio="xMidYMid slice" xmlns="http://www.w3.org/2000/svg">
                  <path d="M-161 679.107L546.107-28l707.103 707.107-707.103 707.103L-161 679.107z" fill="url(#linear3)"
                    fill-opacity=".1" />
                  <defs>
                    <linearGradient id="linear3" x1="192.553" y1="325.553" x2="899.66" y2="1032.66"
                      gradientUnits="userSpaceOnUse">
                      <stop stop-color="#fff" />
                      <stop offset="1" stop-color="#fff" stop-opacity="0" />
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <h3 class="text-lg font-medium text-white">Contact us</h3>
              <p class="mt-6 max-w-3xl text-base text-indigo-50">We are looking forward to hearing from you.</p>
              <dl class="mt-8 space-y-6">
                <dt><span class="sr-only">Phone number</span></dt>
                <dd class="flex text-base text-indigo-50">
                  <PhoneIcon class="h-6 w-6 flex-shrink-0 text-indigo-200" aria-hidden="true" />
                  <span class="ml-3">+1 (868) 395-1206</span>
                </dd>
                <dt><span class="sr-only">Email</span></dt>
                <dd class="flex text-base text-indigo-50">
                  <MailIcon class="h-6 w-6 flex-shrink-0 text-indigo-200" aria-hidden="true" />
                  <span class="ml-3">assistutt@gmail.com</span>
                </dd>
              </dl>
              <ul role="list" class="mt-8 flex space-x-12">
                <li>
                  <a class="text-indigo-200 hover:text-indigo-100" href="https://www.facebook.com/profile.php?id=100087050152606&mibextid=ZbWKwL" target="_blank">
                    <span class="sr-only">Facebook</span>
                    <svg class="h-7 w-7" aria-hidden="true" fill="currentColor" viewBox="0 0 24 24">
                      <path fill-rule="evenodd"
                        d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"
                        clip-rule="evenodd" />
                    </svg>
                  </a>
                </li>
                <li>
                  <a class="text-indigo-200 hover:text-indigo-100" href="https://www.instagram.com/assistu.tt/?igshid=YmM0MjE2YWMzOA==`" target="_blank">
                    <span class="sr-only">Instagram</span>
                    <svg class="h-7 w-7" aria-hidden="true" fill="currentColor" viewBox="0 0 24 24">
                      <path
                        d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" />
                    </svg>
                  </a>
                </li>
              </ul>
            </div>

            <!-- Contact form -->
            <div class="py-10 px-6 sm:px-10 lg:col-span-2 xl:p-12">
              <h3 class="text-lg font-medium text-warm-gray-900">Send us a message</h3>
              <Form v-slot="{ errors }" @submit="OnSubmit" class="mt-6 grid grid-cols-1 gap-y-6 sm:grid-cols-2 sm:gap-x-8">
                <div>
                  <label for="first-name" class="block text-sm font-medium text-warm-gray-900">First name</label>
                  <div class="mt-1">
                    <Field :rules="required" type="text" name="f_name" id="first-name" autocomplete="given-name"
                      class="block w-full rounded-md border-warm-gray-300 py-3 px-4 text-warm-gray-900 shadow-sm focus:border-indigo-500 focus:ring-indigo-500" />
                      <span class="text-red-500 text-sm">{{ errors.f_name }}</span>
                  </div>
                </div>
                <div>
                  <label for="last-name" class="block text-sm font-medium text-warm-gray-900">Last name</label>
                  <div class="mt-1">
                    <Field :rules="required" type="text" name="l_name" id="last-name" autocomplete="family-name"
                      class="block w-full rounded-md border-warm-gray-300 py-3 px-4 text-warm-gray-900 shadow-sm focus:border-indigo-500 focus:ring-indigo-500" />
                      <span class="text-red-500 text-sm">{{ errors.l_name }}</span>
                  </div>
                </div>
                <div>
                  <label for="email" class="block text-sm font-medium text-warm-gray-900">Email</label>
                  <div class="mt-1">
                    <Field :rules="required" id="email" name="email" type="email" autocomplete="email"
                      class="block w-full rounded-md border-warm-gray-300 py-3 px-4 text-warm-gray-900 shadow-sm focus:border-indigo-500 focus:ring-indigo-500" />
                      <span class="text-red-500 text-sm">{{ errors.email }}</span>
                  </div>
                </div>
                <div>
                  <div class="flex justify-between">
                    <label for="phone" class="block text-sm font-medium text-warm-gray-900">Phone</label>
                  </div>
                  <div class="mt-1">
                    <Field :rules="required" type="text" name="phone" id="phone" autocomplete="tel"
                      class="block w-full rounded-md border-warm-gray-300 py-3 px-4 text-warm-gray-900 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
                      aria-describedby="phone-optional" />
                      <span class="text-red-500 text-sm">{{ errors.phone }}</span>
                  </div>
                </div>
                <div class="sm:col-span-2">
                  <div class="flex justify-between">
                    <label for="message" class="block text-sm font-medium text-warm-gray-900">Message</label>
                    <span id="message-max" class="text-sm text-warm-gray-500">Max. 500 characters</span>
                  </div>
                  <div class="mt-1">
                    <Field as="textarea" :rules="required" id="message" name="message" rows="4"
                      class="block w-full rounded-md border-warm-gray-300 py-3 px-4 text-warm-gray-900 shadow-sm focus:border-indigo-500 focus:ring-indigo-500"
                      aria-describedby="message-max" />
                      <span class="text-red-500 text-sm">{{ errors.message }}</span>
                  </div>
                </div>
                <div class="sm:col-span-2 sm:flex sm:justify-end">
                  <button type="submit" :disabled="isLoading"
                    class="mt-2 inline-flex w-full items-center justify-center rounded-md border border-transparent bg-indigo-500 px-6 py-3 text-base font-medium text-white shadow-sm hover:bg-indigo-600 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 sm:w-auto">
                    <svg v-if="isLoading" class="animate-spin -ml-1 mr-3 h-5 w-5 text-white" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                      <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                      <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                    </svg>
                    Submit
                  </button>
                </div>
              </Form>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>



  <TransitionRoot as="template" :show="successful">
    <Dialog as="div" class="relative z-10" @close="successful = false">
      <TransitionChild as="template" enter="ease-out duration-300" enter-from="opacity-0" enter-to="opacity-100" leave="ease-in duration-200" leave-from="opacity-100" leave-to="opacity-0">
        <div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" />
      </TransitionChild>

      <div class="fixed inset-0 z-10 overflow-y-auto">
        <div class="flex min-h-full items-end justify-center p-4 text-center sm:items-center sm:p-0">
          <TransitionChild as="template" enter="ease-out duration-300" enter-from="opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95" enter-to="opacity-100 translate-y-0 sm:scale-100" leave="ease-in duration-200" leave-from="opacity-100 translate-y-0 sm:scale-100" leave-to="opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95">
            <DialogPanel class="relative transform overflow-hidden rounded-lg bg-white px-4 pt-5 pb-4 text-left shadow-xl transition-all sm:my-8 sm:w-full sm:max-w-sm sm:p-6">
              <div>
                <div class="mx-auto flex h-12 w-12 items-center justify-center rounded-full bg-green-100">
                  <CheckIcon class="h-6 w-6 text-green-600" aria-hidden="true" />
                </div>
                <div class="mt-3 text-center sm:mt-5">
                  <DialogTitle as="h3" class="text-lg font-medium leading-6 text-gray-900">Message sent</DialogTitle>
                  <div class="mt-2">
                    <p class="text-sm text-gray-500">Thank you for contacting us. We'll get back to you shortly.</p>
                  </div>
                </div>
              </div>
              <div class="mt-5 sm:mt-6">
                <button type="button" class="inline-flex w-full justify-center rounded-md border border-transparent bg-indigo-600 px-4 py-2 text-base font-medium text-white shadow-sm hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 sm:text-sm" @click="successful = false">Close</button>
              </div>
            </DialogPanel>
          </TransitionChild>
        </div>
      </div>
    </Dialog>
  </TransitionRoot>



  <TransitionRoot as="template" :show="failed">
    <Dialog as="div" class="relative z-10" @close="failed = false">
      <TransitionChild as="template" enter="ease-out duration-300" enter-from="opacity-0" enter-to="opacity-100" leave="ease-in duration-200" leave-from="opacity-100" leave-to="opacity-0">
        <div class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" />
      </TransitionChild>

      <div class="fixed inset-0 z-10 overflow-y-auto">
        <div class="flex min-h-full items-end justify-center p-4 text-center sm:items-center sm:p-0">
          <TransitionChild as="template" enter="ease-out duration-300" enter-from="opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95" enter-to="opacity-100 translate-y-0 sm:scale-100" leave="ease-in duration-200" leave-from="opacity-100 translate-y-0 sm:scale-100" leave-to="opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95">
            <DialogPanel class="relative transform overflow-hidden rounded-lg bg-white px-4 pt-5 pb-4 text-left shadow-xl transition-all sm:my-8 sm:w-full sm:max-w-lg sm:p-6">
              <div class="sm:flex sm:items-start">
                <div class="mx-auto flex h-12 w-12 flex-shrink-0 items-center justify-center rounded-full bg-red-100 sm:mx-0 sm:h-10 sm:w-10">
                  <ExclamationTriangleIcon class="h-6 w-6 text-red-600" aria-hidden="true" />
                </div>
                <div class="mt-3 text-center sm:mt-0 sm:ml-4 sm:text-left">
                  <DialogTitle as="h3" class="text-lg font-medium leading-6 text-gray-900">Oops, something went wrong!</DialogTitle>
                  <div class="mt-2">
                    <p class="text-sm text-gray-500">Looks like we encountered an error. We're sorry for the inconvenience!</p>
                  </div>
                </div>
              </div>
              <div class="mt-5 sm:mt-4 sm:ml-10 sm:flex sm:pl-4">
                <button type="button" class="mt-3 inline-flex w-full justify-center rounded-md border border-gray-300 bg-white px-4 py-2 text-base font-medium text-gray-700 shadow-sm hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 sm:mt-0 sm:ml-3 sm:w-auto sm:text-sm" @click="failed = false" ref="cancelButtonRef">Close</button>
              </div>
            </DialogPanel>
          </TransitionChild>
        </div>
      </div>
    </Dialog>
  </TransitionRoot>



</template>
  
<script setup>
import emailjs from '@emailjs/browser';
import { MailIcon, PhoneIcon, CheckIcon } from '@heroicons/vue/outline/index.js'
import { Field, Form } from 'vee-validate';
import { ref } from 'vue'
import { Dialog, DialogPanel, DialogTitle, TransitionChild, TransitionRoot } from '@headlessui/vue'

const successful = ref(false);
const failed = ref(false);
const isLoading = ref(false);

function required(value) {
  return value ? true : 'This field is required';
}

function OnSubmit(values) {
  isLoading.value = true
  emailjs.send('service_nl955p3','template_uu3m3qe', values, 'DrjNuyJrCutWH4W34')
    .then((response) => {
      successful.value = true;
      isLoading.value = false;
    }, (err) => {
      failed.value = true
      isLoading.value = false;
    });
}

// const plans = {
//   Basic: [
//     'Basic: $899 - 3 months',
//     'Basic: $1799 - 6 months',
//     'Basic: $3699 - 12 months',
//   ],
//   Modern: [
//     'Modern: $1099 - 3 months',
//     'Modern: $2199 - 6 months',
//     'Modern: $4499 - 12 months',
//   ],
//   Elite: [
//     'Elite: $1249 - 3 months',
//     'Elite: $2599 - 6 months',
//     'Elite: $5199 - 12 months',
//   ],
// };
</script>