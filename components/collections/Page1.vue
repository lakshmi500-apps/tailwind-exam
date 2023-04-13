<template>
  <div class="overflow-hidden bg-white py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div
        class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 sm:gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-2"
      >
        <div class="lg:pr-8 lg:pt-4">
          <div class="lg:max-w-lg">
            <p
              class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl"
            >
              Live Chat Software
            </p>
            <h2 class="text-base font-semibold leading-7 text-indigo-600">
              Join the SaaS Revolution - 50 Apps for ₹999
            </h2>

            <dl
              class="mt-10 max-w-xl space-y-4 text-base leading-7 text-gray-600 lg:max-w-none"
            >
              <div
                v-for="feature in features"
                :key="feature.name"
                class="relative pl-9"
              >
                <dt class="inline font-semibold text-gray-900">
                  <CheckIcon
                    :is="feature.icon"
                    class="absolute left-1 top-1 h-5 w-5 text-green-600"
                    aria-hidden="true"
                  />
                </dt>

                <dd class="inline">{{ feature.description }}</dd>
              </div>
              <div class="flex flex-row">
                <a
                  href="#"
                  class="inline-flex rounded-md bg-indigo-600 px-2.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
                >
                  <span>Sign Up</span>
                  <small class="trail-text2 d-block">14-day Trial</small>
                </a>
                <p
                  class="text-or mb-0 my-5 my-md-0 px-4 px-md-5 text-muted font-weight-400"
                >
                  Or
                </p>

                <div class="flex flex-row">
                  <img
                    src=" https://ninjachat.com/lib/images/sso-icons/google.svg?v=1680096338629045558"
                  />
                  <img
                    src="https://ninjachat.com/lib/images/sso-icons/linkedin.svg?v=1680096338629045558"
                  />
                  <img
                    src="https://ninjachat.com/lib/images/sso-icons/microsoft.svg?v=1680096338629045558"
                  />
                  <img
                    src="https://ninjachat.com/lib/images/sso-icons/facebook.svg?v=1680096338629045558"
                  />
                </div>
              </div>
            </dl>
          </div>
        </div>

        <img
          src=" https://res.cloudinary.com/smartsupp/image/upload/w_1200,h_680,c_fill,q_auto,f_auto/v0/upload/mig_gy5unxi4_smartsupp-mobile-app-cover2x.png "
          alt="Product screenshot"
          class="w-[48rem] max-w-none rounded-xl shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem] md:-ml-4 lg:-ml-0 mr-3"
        />
      </div>
    </div>
  </div>
</template>

<script setup>
import {
  CloudArrowUpIcon,
  LockClosedIcon,
  ServerIcon,
  CheckIcon,
} from "@heroicons/vue/20/solid";

const features = [
  {
    description:
      "Convert your visitors with text chat, voice, video, and screen sharing: All-in-one place.",
  },
  {
    description:
      "Engage your visitors by providing them with right information at the right time.",
  },
  {
    description:
      "Create multiple agents and customize the design of your live chat widget.",
  },
  {
    description:
      "Integrate built-in chatbot, BotUp, to assist your customers 24/7.",
  },
  {
    description:
      "Choose the third-party app such as CRM.io or any other CRM software to embed your chat activity.",
  },
];
</script>
