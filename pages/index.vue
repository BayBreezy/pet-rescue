<template>
  <div>
    <div
      class="min-h-screen grid grid-cols-1 lg:grid-cols-2 items-center selection:bg-primary-600 selection:text-white"
    >
      <div class="h-full w-full items-center flex justify-center">
        <div class="g:w-3/4 xl:w-1/2 mx-auto w-11/12 sm:w-8/12">
          <h1 class="md:font-semibold font-medium text-4xl">Welcome back</h1>
          <p class="text-slate-500 mt-3 text-sm mb-20">
            Welcome back! Enter your details to get started.
          </p>
          <form @submit.prevent="">
            <div class="">
              <label
                for="email"
                class="block mb-2 font-medium text-sm text-slate-500 cursor-pointer"
                >Email</label
              >
              <input
                type="email"
                placeholder="Enter your email"
                id="email"
                name="email"
                required
                class="rounded-lg w-full py-3 focus:ring-1 focus:ring-primary-600 focus:outline-none focus:border-transparent valid:border-green-500 border-slate-300"
              />
            </div>
            <div class="mt-7">
              <label
                for="password"
                class="block mb-2 font-medium text-sm text-slate-500 cursor-pointer"
                >Password</label
              >
              <input
                type="password"
                id="password"
                name="password"
                required
                class="rounded-lg w-full py-3 focus:ring-1 focus:ring-primary-600 focus:outline-none focus:border-transparent valid:border-green-500 border-slate-300"
              />
            </div>
            <div class="mt-7">
              <div>
                <nuxt-link to="/#forgot-password" class="text-xs text-slate-400"
                  >Forgot password?
                </nuxt-link>
              </div>
            </div>
            <div class="mt-3">
              <button
                type="submit"
                class="focus:outline-none transition-all duration-300 py-3 w-full text-sm bg-primary-700 rounded-lg text-white hover:shadow-xl hover:shadow-primary-300"
              >
                Login
              </button>
            </div>
            <div class="mt-6">
              <button
                type="button"
                class="outline-none transition-all duration-300 py-3 w-full text-sm rounded-lg flex items-center justify-center border hover:border-primary-400"
              >
                <img
                  src="/google.svg"
                  alt="Google Icon"
                  class="object-cover w-6 h-6"
                />
                <span class="ml-2"> Sign in with Google </span>
              </button>
            </div>
          </form>
          <div class="mt-6">
            <div>
              <nuxt-link to="/register" class="text-xs text-slate-400"
                >Don't have an account?
                <span
                  class="underline decoration-primary-500 decoration-wavy text-primary-600"
                  >Register here</span
                ></nuxt-link
              >
            </div>
          </div>
        </div>
      </div>
      <div
        class="h-full w-full bg-[url('/login.jpg')] bg-no-repeat bg-cover bg-center hidden lg:flex justify-center items-end"
      >
        <Review />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>
