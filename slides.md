---
theme: unicorn
colorSchema: "dark"
layout: cover
logoHeader: "https://eva.guru/wp-content/uploads/2022/08/white-eva-logopodcas.png"
website: "eva.guru"
class: "text-center"
---
# Why we should upgrade Eva?

<div class="flex items-center justify-center gap-12">
  <img class="w-[64px] h-[64px]" src="/logos/pinia.svg" />
  <img class="w-[64px] h-[64px]" src="/logos/vue.png" />
  <img class="w-[64px] h-[64px]" src="/logos/vueuse.svg" />
  <img class="w-[72px] h-[72px]" src="/logos/tailwind.svg" />
</div>

---
class: 'text-center'
---
# Because, please

<div class="flex items-center justify-center">
  <img src="/please.gif" />
</div>

---
layout: cover
---
# Package Version Reasons

Reasons why we should upgrade Eva to new Tech Stack

<div class="text-2xl flex flex-col gap-2">
  <span class="flex gap-4 items-center"><logos-vue class="h-[24px] w-[24px]" /> <strong>Vue 3</strong> has cleaner syntax, has up-to-date API, perfect TS integration.</span>
  <span class="flex gap-4 items-center"><logos-vitejs class="text-4xl" /> <span><strong>Vite</strong> has first-class integration with Vite. It uses esbuild for development server, which is ~100 times faster than webpack in cold-starts and HMR.</span></span>
  <span class="flex gap-4 items-center">
  <img class="w-[32px] h-[32px]" src="/logos/pinia.svg" /> <span><strong>Pinia</strong> has solid type inference, removes mutations completely, import the actions and then use it <twemoji-partying-face class="text-base" /></span></span>
  <span class="flex gap-4 items-center">
  <logos-typescript-icon class="text-4xl" /> <span><strong>TypeScript</strong> is a must in project that complex. We should take advantage of things such as 'autocompletion', 'symbol renaming', 'refactor confidence'.</span></span>
  <span class="flex gap-4 items-center">
  <img class="w-[24px] h-[24px]" src="/logos/vueuse.svg" /> <span><strong>VueUse</strong> provides tons of utilites and has great support for Vue3 and TypeScript.</span></span>
</div>

---
layout: center
---
# What will upgrading all of this brings us?

---
layout: cover
---
# Decreased Build/Development Server Start Time


<div class="flex flex-col gap-3 my-4">
  <span>Vue2 + Webpack (~120s total)</span>
  <div>
  <img class="h-[300px] w-auto" src="/buildvue2.png" />
  </div>
  <small>This results are from my local machine. <twemoji-man-shrugging class="text-2xl" /></small>
</div>

---
layout: cover
---
# Decreased Build/Development Server Start Time

<div class="flex flex-col gap-3 my-4">
  <span>Vue3 + Vite + Typescript Compile (~2.4s total)</span>
  <div>
  <img class="w-auto" src="/buildvue3.png" />
  </div>
  <small>Similar project</small>
</div>

---
layout: cover
---
# Type Safety

<div class="flex flex-col gap-3 my-4">
  <span>Wouldn't be great if we move from this</span>
  <div>
  <img class="h-[300px] w-auto" src="/jsversion.png" />
  </div>
</div>

---
layout: cover
---
# Type Safety

<div class="flex flex-col gap-3 my-4">
  <span>To this. Autocompletion gives confidency and speeds up developer at least 2 times.</span>
  <div>
  <img class="h-[300px] w-auto" src="/tsversion.png" />
  </div>
</div>

---
layout: cover
---

# Removing Mutations

<div class="flex flex-col gap-3 my-4">
  <span>Vue2 + Vuex</span>
  <div>
    <img class="h-[300px] w-auto" src="/vuex.png" />
  </div>
  <small>What this action do? Is this action exist? Is this parametes are correct? We can't use go to definition.</small>
</div>

---
layout: cover
---

# Removing Mutations

<div class="flex flex-col gap-3 my-4">
  <span>Vue3 + Pinia</span>
  <div>
    <img class="h-[300px] w-auto" src="/pinia.png" />
  </div>
  <small>We can see what this action do, just by clicking it. We have autocomplete for parameters.</small>
</div>

---
layout: cover
---

# Removing Unused, Outdated Dependencies

Just small portion of our dependencies

```json {3|4|5|6|7|8|9|10|11|12|15|16}
{
 "dependencies": {
    "auth0-js": "^9.10.4", // unused
    "axios": "^0.19.0", // v1.3 is available, we are using pre stable version
    "file-saver": "^2.0.2", // outdated
    "highcharts": "^8.1.2", // v10.3 is available 
    "jsonwebtoken": "^8.5.1", // v9.0 is available with security fixes
    "lodash": "^4.17.21", // we can use tree-shakable lodash-es
    "moment-timezone": "^0.5.31", // moment is deprecated
    "vue": "^2.6.10", // Don't much to say
    "vuesax": "jd-0001/vuesax", // just outdated
    "vuex": "^3.1.1", // v4.1 is available, also its deprecated in favor of Pinia
  },
  "devDependencies": {
    "purgecss": "^1.3.0", // v5.0 is available with tons of improvements
    "tailwindcss": "^1.0.1" // v3.1 is available with tons of improvements
  }
}
```

Removing or upgrading won't simply work. We have incompatibilities in nearly every dependency.

---
layout: cover
---

# Decreasing File Sizes

<div class="flex flex-col gap-3 my-4">
  <span>Repricer Main Page (~1MB)</span>
  <div>
    <img class="h-[300px] w-auto" src="/repricer.png" />
  </div>
  <small>Just 1 character change in repricer page takes ~4-5s for HMR. It's both Webpack's and bad structures fault.</small>
</div>

---
layout: cover
---

# Opinionated Folder Structure

<div class="flex flex-col gap-3 my-4">
  <span>What is components folder by the way?</span>
  <div class="flex gap-6 mt-4">
    <img class="h-[300px] w-[20%]" src="/structure1.png" />
    <img class="h-[300px] w-[20%]" src="/structure2.png" />
    <img class="h-[300px] w-[20%]" src="/structure3.png" />
    <img class="h-[300px] w-[20%]" src="/structure4.png" />
  </div>
  <small>It's just confusing and hard to maintain.</small>
</div>

---
layout: cover
---

# Strict Linting and Formatting

<div class="flex flex-col gap-3 my-4">
  <span>We are using Eslint, but pushing code without fixing linting errors is allowed. It seems too late to fix all of them.</span>
  <div>
    <img class="h-[300px] w-auto" src="/lint.png" />
  </div>
  <small>After we decide to move new project, we can discuss about linting rules and formatting, and have strict rules for pushing code to production.</small>
</div>

---
layout: cover
---

# Adding Tests

In current state, it's just too complicated to add tests. Either because of the complexity of the project or the fact that we have to rely on outdated testing libraries.

## Vitest For Unit Tests

<logos-vitest class="text-9xl" />

We can use Vite's test runner for Unit Tests.

It's fast, easy to use and has great support for Vue3.

After adding tests, we can deploy production even in the middle of the night without worrying about breaking something.

---
layout: cover
---

# Adding Tests

In current state, it's just too complicated to add tests. Either because of the complexity of the project or the fact that we have to rely on outdated testing libraries.

## Playwright For E2E Tests

<logos-playwright class="text-9xl" />

We can use Playwright for E2E Tests.

It's fast, supports all major browsers, great support for Vue 3. No more worry about browser compatibility!

After adding tests, we can deploy production even in the middle of the night without worrying about breaking something.

---
layout: cover
---

# Storybook

<div class="flex flex-col gap-3 my-4">
  <span>Storybook is a great tool for developing UI components in isolation. It's like Swagger for Frontend. We can have Component Library preview tool for our P.O.'s, UI/UX designers and they can test components directly in browser just by changing props.</span>
  <div>
    <img class="h-[300px] w-auto" src="/storybook.png" />
  </div>
</div>

---
layout: cover
---

# VueUse

<div class="flex flex-col gap-3 my-4">
  <span>VueUse is a perfect tool for adding functionality to Vue3. It's like configurable lodash for Vue3. We can add functionality to Vue3 without adding extra dependencies.</span>

  ```ts
  import { onClickOutside } from '@vueuse/core'

  const ref = ref<HTMLDivElement>(null)

  onClickOutside(ref, () => {
    console.log('clicked outside')
  });
  ```
</div>

---
layout: cover
---

# VueUse

<div class="flex flex-col gap-3 my-4">
  <span>There are 200+ composition functions, all three-shakable, rich TypeScript support and great documentation.</span>

  <div class="flex gap-6 mt-4">
    <img class="h-[300px] w-auto" src="/vueuse1.png" />
    <img class="h-[300px] w-auto" src="/vueuse2.png" />
    <img class="h-[300px] w-auto" src="/vueuse3.png" />
    <img class="h-[300px] w-auto" src="/vueuse4.png" />
    <img class="h-[300px] w-auto" src="/vueuse5.png" />
  </div>
  
  <small>Few examples of VueUse composition functions.</small>
</div>

---
layout: cover
---

# Other Topics

<v-clicks>

- **Easier to find solutions online.** New libraries and tools have great documentation and have active community. We can easily find solutions for our problems.
- **Easier to improve.** With new libraries and tools, we can easily add new features to our project. Now, new features are hard to add because of the complexity of the project. This will increase our productivity and speed up delivery times.
- **Easier to onboard for new developers.** Becuase we will have a clean codebase, strict linting rules, storybooks and tests! New developers will be able to understand the codebase easily.
- **Easier to maintain.** We can fix production bugs or refactor our code easily. Rename a variable? Just press F2. It's that easy.
- **Easier to scaling up.** We can have code-splitting after adding new features. We can add new features without worrying about bundle size. When someone goes our app for the first time, its now serving 12MB data. Its terrible for user experience.
- **Easier to hire new developers.** Nowadays, it's hard to find developers who are familiar with old libraries and tools. We can easily hire new developers with new libraries and tools.
  
</v-clicks>

---
layout: cover
---

# Summary

We covered a lot of topics in this talk. There are one more thing that I want to talk about.

**Developer Experience.**

---
layout: center
--- 

# Thanks For Listening!