<script>
    let openIndex = null;
  
    function toggle(index) {
      openIndex = openIndex === index ? null : index;
    }
  </script>
  
  <section class="w-full py-12 md:py-24 lg:py-32 bg-gray-900">
    <div class="container mx-auto px-4 md:px-6 space-y-12">
      <div class="text-center">
        <h2 class="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl text-white">
          FAQ
        </h2>
      </div>
      <div class="space-y-6">
        <!-- Static FAQ items -->
        <div>
          <button
            class="flex items-center justify-between w-full px-4 py-3 bg-gray-800 rounded-md cursor-pointer transition-all duration-300 ease-in-out hover:bg-gray-700"
            aria-expanded={openIndex === 0}
            aria-controls="faq-1"
            on:click={() => toggle(0)}
          >
            <h3 class="text-lg font-medium text-white">
              What is this product?
            </h3>
            <svg
              class={`w-6 h-6 text-gray-400 transform transition-transform duration-300 ease-in-out ${openIndex === 0 ? 'rotate-180' : ''}`}
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div
            id="faq-1"
            class={`px-4 py-3 text-gray-300 bg-gray-800 rounded-md mt-2 transition-all duration-300 ease-in-out overflow-hidden ${openIndex === 0 ? 'max-h-screen' : 'max-h-0'}`}
          >
            This is a powerful platform that enables companies of all sizes to create at the moment of inspiration. It provides a complete set of tools and services to build, deploy, and scale web applications.
          </div>
        </div>
  
        <div>
          <button
            class="flex items-center justify-between w-full px-4 py-3 bg-gray-800 rounded-md cursor-pointer transition-all duration-300 ease-in-out hover:bg-gray-700"
            aria-expanded={openIndex === 1}
            aria-controls="faq-2"
            on:click={() => toggle(1)}
          >
            <h3 class="text-lg font-medium text-white">
              How does it work?
            </h3>
            <svg
              class={`w-6 h-6 text-gray-400 transform transition-transform duration-300 ease-in-out ${openIndex === 1 ? 'rotate-180' : ''}`}
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div
            id="faq-2"
            class={`px-4 py-3 text-gray-300 bg-gray-800 rounded-md mt-2 transition-all duration-300 ease-in-out overflow-hidden ${openIndex === 1 ? 'max-h-screen' : 'max-h-0'}`}
          >
            Our platform provides a seamless workflow for building and deploying web applications. It includes features like automated CI/CD, built-in testing, and integrated collaboration tools to help your team focus on shipping features instead of managing infrastructure.
          </div>
        </div>
  
        <div>
          <button
            class="flex items-center justify-between w-full px-4 py-3 bg-gray-800 rounded-md cursor-pointer transition-all duration-300 ease-in-out hover:bg-gray-700"
            aria-expanded={openIndex === 2}
            aria-controls="faq-3"
            on:click={() => toggle(2)}
          >
            <h3 class="text-lg font-medium text-white">
              What are the key features?
            </h3>
            <svg
              class={`w-6 h-6 text-gray-400 transform transition-transform duration-300 ease-in-out ${openIndex === 2 ? 'rotate-180' : ''}`}
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div
            id="faq-3"
            class={`px-4 py-3 text-gray-300 bg-gray-800 rounded-md mt-2 transition-all duration-300 ease-in-out overflow-hidden ${openIndex === 2 ? 'max-h-screen' : 'max-h-0'}`}
          >
            <ul class="space-y-2">
              <li>Infinite scalability with zero config</li>
              <li>Real-time insights and controls</li>
              <li>Personalization at the edge</li>
              <li>Automated CI/CD and built-in testing</li>
              <li>Integrated collaboration tools</li>
            </ul>
          </div>
        </div>
  
        <div>
          <button
            class="flex items-center justify-between w-full px-4 py-3 bg-gray-800 rounded-md cursor-pointer transition-all duration-300 ease-in-out hover:bg-gray-700"
            aria-expanded={openIndex === 3}
            aria-controls="faq-4"
            on:click={() => toggle(3)}
          >
            <h3 class="text-lg font-medium text-white">
              How much does it cost?
            </h3>
            <svg
              class={`w-6 h-6 text-gray-400 transform transition-transform duration-300 ease-in-out ${openIndex === 3 ? 'rotate-180' : ''}`}
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div
            id="faq-4"
            class={`px-4 py-3 text-gray-300 bg-gray-800 rounded-md mt-2 transition-all duration-300 ease-in-out overflow-hidden ${openIndex === 3 ? 'max-h-screen' : 'max-h-0'}`}
          >
            We offer flexible pricing plans to fit the needs of businesses of all sizes. Pricing starts at $99 per month for our Starter plan, with additional tiers available for growing teams and enterprises. You can find more details on our pricing page.
          </div>
        </div>
  
        <div>
          <button
            class="flex items-center justify-between w-full px-4 py-3 bg-gray-800 rounded-md cursor-pointer transition-all duration-300 ease-in-out hover:bg-gray-700"
            aria-expanded={openIndex === 4}
            aria-controls="faq-5"
            on:click={() => toggle(4)}
          >
            <h3 class="text-lg font-medium text-white">
              How do I get started?
            </h3>
            <svg
              class={`w-6 h-6 text-gray-400 transform transition-transform duration-300 ease-in-out ${openIndex === 4 ? 'rotate-180' : ''}`}
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </button>
          <div
            id="faq-5"
            class={`px-4 py-3 text-gray-300 bg-gray-800 rounded-md mt-2 transition-all duration-300 ease-in-out overflow-hidden ${openIndex === 4 ? 'max-h-screen' : 'max-h-0'}`}
          >
            Getting started is easy! Simply sign up for a free account on our website and you can start building and deploying your web applications right away. Our documentation and support team are here to help you every step of the way.
          </div>
        </div>
      </div>
    </div>
  </section>
  