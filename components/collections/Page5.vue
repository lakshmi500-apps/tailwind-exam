<template>
    <div class="bg-white py-24 sm:py-32">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-4xl text-center">
          <p
            class="mt-2 text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl"
          >
            One Pricing for <span class="bg-amber-300">50 Apps</span> at just ₹999
          </p>
          <h2 class="text-base font-semibold leading-7 text-slate-400">
            Honest pricing. Cancel anytime.
          </h2>
        </div>
        <div class="flex items-center justify-center mt-5 mb-0">
          <span class="text-sm mr-2">Monthly</span>
  
  
          <Switch
            v-model="enabled"
            :class="[
              enabled ? 'bg-indigo-600' : 'bg-gray-200',
              'relative inline-flex h-6 w-11 flex-shrink-0 cursor-pointer rounded-full border-2 border-transparent transition-colors duration-200 ease-in-out focus:outline-none focus:ring-2 focus:ring-indigo-600 focus:ring-offset-2',
            ]"
          >
            <span class="sr-only">Use setting</span>
            <span
              aria-hidden="true"
              :class="[
                enabled ? 'translate-x-5' : 'translate-x-0',
                'pointer-events-none inline-block h-5 w-5 transform rounded-full bg-white shadow ring-0 transition duration-200 ease-in-out',
              ]"
            />
          </Switch>
          <span class="small ty_spanText mr-2"> Yearly </span>
        </div>
        <div
          class="isolate mx-auto mt-16 grid max-w-md grid-cols-1 gap-y-8 sm:mt-20 lg:mx-0 lg:max-w-none lg:grid-cols-3"
        >
          <div
            v-for="(tier, tierIdx) in tiers"
            :key="tier.id"
            :class="[
              tier.mostPopular ? 'lg:z-10 lg:rounded-b-none' : 'lg:mt-8',
              tierIdx === 0 ? 'lg:rounded-r-none' : '',
              tierIdx === tiers.length - 1 ? 'lg:rounded-l-none' : '',
              'flex flex-col justify-between rounded-3xl bg-white p-8 ring-1 ring-gray-200 xl:p-10',
            ]"
          >
            <div>
              <div class="flex items-center justify-between gap-x-4">
                <h3
                  :id="tier.id"
                  :class="[
                    tier.mostPopular ? 'text-indigo-600' : 'text-gray-900',
                    'text-lg font-semibold leading-8',
                  ]"
                >
                  {{ tier.name }}
                </h3>
                <p
                  v-if="tier.mostPopular"
                  class="rounded-full bg-indigo-600/10 px-2.5 py-1 text-xs font-semibold leading-5 text-indigo-600"
                >
                  Recommended
                </p>
              </div>
              <p class="mt-4 text-sm leading-6 text-gray-600">
                {{ tier.description }}
              </p>
              <p class="mt-6 flex items-baseline gap-x-1">
                <span class="text-4xl font-bold tracking-tight text-gray-900">{{
                  tier.priceMonthly
                }}</span>
                <span
                  class="text-sm font-semibold leading-6 text-gray-600"
                  v-if="!tier.name == 'Hosted'"
                  >/month</span
                >
              </p>
              <ul
                role="list"
                class="mt-8 space-y-3 text-sm leading-6 text-gray-600"
              >
                <li
                  v-for="feature in tier.features"
                  :key="feature"
                  class="flex gap-x-3"
                >
                  <CheckIcon
                    class="h-6 w-5 flex-none text-indigo-600"
                    aria-hidden="true"
                  />
                  {{ feature }}
                </li>
              </ul>
            </div>
            <div>
              <div v-if="tier.name == 'Hosted'">
                <dl class="mt-5">
                  <div
                    class="relative overflow-hidden rounded-lg bg-gray-900 px-4 pb-12 pt-5 flex flex-col text-center"
                  >
                    <p class="text-amber-400">Bring Your Own Server</p>
                    <button class="bg-white p-2 rounded-lg w-full">
                      Contact Us for Pricing
                    </button>
                    <p class="text-gray-400">Yearly Subscription</p>
                  </div>
                </dl>
              </div>
              <a
                v-else
                :href="tier.href"
                :aria-describedby="tier.id"
                :class="[
                  tier.mostPopular
                    ? 'bg-indigo-600 text-white shadow-sm hover:bg-indigo-500'
                    : 'text-indigo-600 ring-1 ring-inset ring-indigo-200 hover:ring-indigo-300',
                  'mt-8 block rounded-md py-2 px-3 text-center text-sm font-semibold leading-6 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600',
                ]"
                >Sign Up
                <span class="flex-col md:flex text-gray-700"
                  >14-day Trail</span
                ></a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  
  <script setup>
  import { CheckIcon } from "@heroicons/vue/20/solid";
  import { ref } from "vue";
  import { Switch } from "@headlessui/vue";
  
  
  const enabled = ref(true);
  const tiers = [
    {
      name: "Cloud",
      id: "tier-freelancer",
      href: "#",
      priceMonthly: "$24",
      description: "The essentials to provide your best work for clients.",
      features: [
        "50 apps (Hosted in 6 locations)",
        "99.5% Guaranteed Global Uptime",
        "24/5 Email, Chat Support",
        "Multiple Workspaces",
        "No Feature Caps",
      ],
      mostPopular: false,
    },
    {
      name: "Enterprise",
      id: "tier-startup",
      href: "#",
      priceMonthly: "$32",
      description: "A plan that scales with your rapidly growing business.",
      features: [
        "50 apps (Hosted in 6 locations)",
        "99.99% Guaranteed Global Uptime",
        "24/5 Email, Chat and Phone Support",
        "Dedicated Account Representative",
        "Minimum 25 users",
        "Personalized Onboarding",
        "White Label ?",
        "Extra Security and Compliance",
      ],
      mostPopular: true,
    },
    {
      name: "Hosted",
      id: "tier-enterprise",
      href: "#",
  
  
      description:
        "Use 500apps in your infrastructure for extra security and compliance",
      features: [
        "White Label ?",
        "BYOS (Bring Your Own Server)",
        "Hosted Locally on your Server",
        "100% On-premises Solutions",
        "99.99% Guaranteed Global Uptime",
      ],
      mostPopular: false,
    },
  ];
  </script>