<template class="">
  <header
    class="fixed block w-full bg-[#CFE1F5] backdrop-filter backdrop-blur-sm bg-opacity-10 dark:backdrop-filter dark:backdrop-blur-sm dark:bg-opacity-10 dark:bg-[#17191dce] top-0"
  >
    <div class="flex justify-between items-center p-6 h-[8vh]">
      <div>
        <img src="@/assets/icons/the2.png" class="w-11" />
      </div>

      <div>
        <svg
          v-if="!isDarkMode"
          @click="toggleDarkMode"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="black"
          class="w-6 aspect-square"
        >
          <g class="theme-toggle-sun">
            <path
              class="theme-toggle__status theme-toggle__moon"
              d="M9.528 1.718a.75.75 0 01.162.819A8.97 8.97 0 009 6a9 9 0 009 9 8.97 8.97 0 003.463-.69.75.75 0 01.981.98 10.503 10.503 0 01-9.694 6.46c-5.799 0-10.5-4.701-10.5-10.5 0-4.368 2.667-8.112 6.46-9.694a.75.75 0 01.818.162z"
            ></path>
          </g>
        </svg>
        <svg
          v-else
          @click="toggleDarkMode"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          fill="white"
          class="w-6 aspect-square"
        >
          <g
            class="transform-box-fill transform origin-center scale-[var(--icon-scale)] translate-y-[var(--icon-translate)]"
          >
            <path
              class="theme-toggle__status theme-toggle__sun"
              d="M12 2.25a.75.75 0 01.75.75v2.25a.75.75 0 01-1.5 0V3a.75.75 0 01.75-.75zM7.5 12a4.5 4.5 0 119 0 4.5 4.5 0 01-9 0zM18.894 6.166a.75.75 0 00-1.06-1.06l-1.591 1.59a.75.75 0 101.06 1.061l1.591-1.59zM21.75 12a.75.75 0 01-.75.75h-2.25a.75.75 0 010-1.5H21a.75.75 0 01.75.75zM17.834 18.894a.75.75 0 001.06-1.06l-1.59-1.591a.75.75 0 10-1.061 1.06l1.59 1.591zM12 18a.75.75 0 01.75.75V21a.75.75 0 01-1.5 0v-2.25A.75.75 0 0112 18zM7.758 17.303a.75.75 0 00-1.061-1.06l-1.591 1.59a.75.75 0 001.06 1.061l1.591-1.59zM6 12a.75.75 0 01-.75.75H3a.75.75 0 010-1.5h2.25A.75.75 0 016 12zM6.697 7.757a.75.75 0 001.06-1.06l-1.59-1.591a.75.75 0 00-1.061 1.06l1.59 1.591z"
            ></path>
            // eslint-disable-next-line prettier/prettier
          </g>
        </svg>
      </div>
    </div>
  </header>
  <router-view />
  <div class="dark:bg-bgcolor dark:text-white h-full pt-12">
    <div class="w-[30vh] m-auto">
      <div class="flex justify-between">
        <svg
          @click="linkedIn"
          fill="currentColor"
          class="w-5 h-5 hover:cursor-pointer"
          viewBox="0 0 20 20"
          role="img"
        >
          <title>Rss icon</title>
          <path
            d="M3.75 3a.75.75 0 00-.75.75v.5c0 .414.336.75.75.75H4c6.075 0 11 4.925 11 11v.25c0 .414.336.75.75.75h.5a.75.75 0 00.75-.75V16C17 8.82 11.18 3 4 3h-.25z"
          ></path>
          <path
            d="M3 8.75A.75.75 0 013.75 8H4a8 8 0 018 8v.25a.75.75 0 01-.75.75h-.5a.75.75 0 01-.75-.75V16a6 6 0 00-6-6h-.25A.75.75 0 013 9.25v-.5zM7 15a2 2 0 11-4 0 2 2 0 014 0z"
          ></path>
        </svg>
        <svg
          @click="twitter"
          fill="currentColor"
          class="w-5 h-5 hover:cursor-pointer"
          viewBox="0 0 24 24"
          role="img"
        >
          <title>Twitter icon</title>
          <path
            d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"
          ></path>
        </svg>
        <svg
          @click="instagram"
          fill="currentColor"
          role="img"
          class="w-5 h-5 hover:cursor-pointer"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <title>Instagram icon</title>
          <path
            d="M12 0C8.74 0 8.333.015 7.053.072 5.775.132 4.905.333 4.14.63c-.789.306-1.459.717-2.126 1.384S.935 3.35.63 4.14C.333 4.905.131 5.775.072 7.053.012 8.333 0 8.74 0 12s.015 3.667.072 4.947c.06 1.277.261 2.148.558 2.913.306.788.717 1.459 1.384 2.126.667.666 1.336 1.079 2.126 1.384.766.296 1.636.499 2.913.558C8.333 23.988 8.74 24 12 24s3.667-.015 4.947-.072c1.277-.06 2.148-.262 2.913-.558.788-.306 1.459-.718 2.126-1.384.666-.667 1.079-1.335 1.384-2.126.296-.765.499-1.636.558-2.913.06-1.28.072-1.687.072-4.947s-.015-3.667-.072-4.947c-.06-1.277-.262-2.149-.558-2.913-.306-.789-.718-1.459-1.384-2.126C21.319 1.347 20.651.935 19.86.63c-.765-.297-1.636-.499-2.913-.558C15.667.012 15.26 0 12 0zm0 2.16c3.203 0 3.585.016 4.85.071 1.17.055 1.805.249 2.227.415.562.217.96.477 1.382.896.419.42.679.819.896 1.381.164.422.36 1.057.413 2.227.057 1.266.07 1.646.07 4.85s-.015 3.585-.074 4.85c-.061 1.17-.256 1.805-.421 2.227-.224.562-.479.96-.899 1.382-.419.419-.824.679-1.38.896-.42.164-1.065.36-2.235.413-1.274.057-1.649.07-4.859.07-3.211 0-3.586-.015-4.859-.074-1.171-.061-1.816-.256-2.236-.421-.569-.224-.96-.479-1.379-.899-.421-.419-.69-.824-.9-1.38-.165-.42-.359-1.065-.42-2.235-.045-1.26-.061-1.649-.061-4.844 0-3.196.016-3.586.061-4.861.061-1.17.255-1.814.42-2.234.21-.57.479-.96.9-1.381.419-.419.81-.689 1.379-.898.42-.166 1.051-.361 2.221-.421 1.275-.045 1.65-.06 4.859-.06l.045.03zm0 3.678c-3.405 0-6.162 2.76-6.162 6.162 0 3.405 2.76 6.162 6.162 6.162 3.405 0 6.162-2.76 6.162-6.162 0-3.405-2.76-6.162-6.162-6.162zM12 16c-2.21 0-4-1.79-4-4s1.79-4 4-4 4 1.79 4 4-1.79 4-4 4zm7.846-10.405c0 .795-.646 1.44-1.44 1.44-.795 0-1.44-.646-1.44-1.44 0-.794.646-1.439 1.44-1.439.793-.001 1.44.645 1.44 1.439z"
          ></path>
        </svg>
        <svg
          @click="instagram"
          fill="currentColor"
          class="w-5 h-5 hover:cursor-pointer"
          viewBox="0 0 24 24"
          role="img"
        >
          <title>Github icon</title>
          <path
            d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"
          ></path>
        </svg>
      </div>
      <p
        class="text-[#868e96] text-sm flex justify-center mt-4 tracking-tighter pb-7"
      >
        jsWithTola © 2024
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, onMounted, ref } from "vue";
// import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

export default defineComponent({
  name: "HomeView",
  components: {},
  setup(props, ctx) {
    const tabs = ref(["Feed", "About", "Project", "Reviews"]);
    const active = ref("Feed");
    const isActive = (type: any) => {
      active.value = type;
    };
    const instagram = () => {
      window.open("https://www.instagram.com/jswithtola/", "_blank");
    };
    const twitter = () => {
      window.open("https://x.com/giwafauzziyyah", "_blank");
    };
    const gitHub = () => {
      window.open("https://github.com/tolani-dev", "_blank");
    };
    const linkedIn = () => {
      window.open("www.linkedin.com/in/giwafauzziyyah", "_blank");
    };
    const isDarkMode = ref(false);

    // Function to toggle dark mode
    const toggleDarkMode = () => {
      console.log("dark");
      isDarkMode.value = !isDarkMode.value;
      if (isDarkMode.value) {
        document.documentElement.classList.add("dark");
        localStorage.setItem("theme", "dark");
      } else {
        document.documentElement.classList.remove("dark");
        localStorage.setItem("theme", "light");
      }
    };
    // Check the user's theme preference on mounted
    onMounted(() => {
      const storedTheme = localStorage.getItem("theme");
      const userPrefersDark = window.matchMedia(
        "(prefers-color-scheme: dark)"
      ).matches;
      if (storedTheme === "dark" || (!storedTheme && userPrefersDark)) {
        isDarkMode.value = true;
        document.documentElement.classList.add("dark");
      }
    });
    return {
      tabs,
      isActive,
      active,
      instagram,
      twitter,
      gitHub,
      linkedIn,
      toggleDarkMode,
      isDarkMode,
    };
  },
});
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  min-height: 100vh;
  /* color: white; */
  /* background-color: #17191d !important; */
}
svg {
  /* color: white; */
}
</style>
