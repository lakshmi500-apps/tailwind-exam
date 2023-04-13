<template>
   
        <div class="py-24 sm:py-32 lg:pb-40">
          <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="mx-auto max-w-2xl text-center">
              <h1 class="text-2xl font-bold tracking-tight text-gray-900 sm:text-6xl">Powerful Features</h1>
              <p class="mt-6 text-lg leading-8 text-gray-600">Limitless Possibilities. What will you do for your business?</p>
              
            </div>
            <div v-for="feature in features" :key="feature.name" class="relative pl-9">
                <dt class="inline font-semibold text-gray-900">
                  <CheckIcon :is="feature.icon" class="absolute left-1 top-1 h-5 w-5 text-green-600" aria-hidden="true" />
                
                </dt>
              
                <dd class="inline">{{ feature.description }}</dd>
                            </div>
            <div class="mt-16 flow-root sm:mt-16">
              <div class="-m-2 rounded-xl bg-gray-900/5 p-2 ring-1 ring-inset ring-gray-900/10 lg:-m-4 lg:rounded-2xl lg:p-4">
                <img src="https://ninjachat.com/images/website-live-chat-screenshot.png" alt="App screenshot" width="400" height="400" class="rounded-md shadow-2xl ring-1 ring-gray-900/10" />
              </div>
            </div>
          </div>
        </div>
        <dl
              class="mt-10 max-w-xl space-y-4 text-base leading-7 text-gray-600 lg:max-w-none"
            >
        <div class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
          <div class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
        </div>
    </dl>
  </template>
  <script>
  const features = [
  {
    
    description:
      'Convert your visitors with text chat, voice, video, and screen sharing: All-in-one place.',
    
  },
  {
    
    description:
      'Engage your visitors by providing them with right information at the right time.',
  
  },
  {
   
    description: 'Create multiple agents and customize the design of your live chat widget.',
    
  },
  {
    
    description: 'Integrate built-in chatbot, BotUp, to assist your customers 24/7.',
    
  },
  {
    
    description: 'Choose the third-party app such as CRM.io or any other CRM software to embed your chat activity.',
    
  },
]
</script>
  
  