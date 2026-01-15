<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup>
useHead({
  script: [
    {
      src: 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/js/all.min.js',
      crossorigin: 'anonymous',
      referrerpolicy: 'no-referrer'
    }
  ]
})
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800;900&display=swap');

html {
  scroll-behavior: smooth;
}

body {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

::-webkit-scrollbar {
  display: none;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.gradient-animate {
  background-size: 200% 200%;
  animation: gradient 5s ease infinite;
}

:root {
  /* Base colors */
    /* Base colors */
    --color-base: #ffffff;
    --color-base-50: #f9fafb;
    --color-base-100: #f3f4f6;
    --color-base-200: #e5e7eb;
    --color-base-300: #d1d5db;
    --color-base-400: #9ca3af;
    --color-base-500: #6b7280;
    --color-base-600: #4b5563;
    --color-base-700: #374151;
    --color-base-800: #1f2937;
    --color-base-900: #111827;
    --color-base-content: #1f2937;

    /* Primary colors - Cedar Green */
    --color-primary: #2D5A3D;
    --color-primary-50: #f0f7f2;
    --color-primary-100: #d9ebe0;
    --color-primary-200: #b3d7c1;
    --color-primary-300: #8dc3a2;
    --color-primary-400: #4a8a5e;
    --color-primary-500: #2D5A3D;
    --color-primary-600: #264d34;
    --color-primary-700: #1f402b;
    --color-primary-800: #183322;
    --color-primary-900: #112619;
    --color-primary-focus: #264d34;
    --color-primary-content: #ffffff;

    /* Secondary colors - Cedar Brown/Wood */
    --color-secondary: #5D4037;
    --color-secondary-50: #EFEBE9;
    --color-secondary-100: #D7CCC8;
    --color-secondary-200: #BCAAA4;
    --color-secondary-300: #A1887F;
    --color-secondary-400: #8D6E63;
    --color-secondary-500: #795548;
    --color-secondary-600: #6D4C41;
    --color-secondary-700: #5D4037;
    --color-secondary-800: #4E342E;
    --color-secondary-900: #3E2723;
    --color-secondary-focus: #4E342E;
    --color-secondary-content: #ffffff;

    /* Accent colors */
    --color-accent: #f472b6;
    --color-accent-50: #fdf2f8;
    --color-accent-100: #fce7f3;
    --color-accent-200: #fbcfe8;
    --color-accent-300: #f9a8d4;
    --color-accent-400: #f472b6;
    --color-accent-500: #ec4899;
    --color-accent-600: #db2777;
    --color-accent-700: #be185d;
    --color-accent-800: #9d174d;
    --color-accent-900: #831843;
    --color-accent-focus: #db2777;
    --color-accent-content: #ffffff;

    /* Neutral colors */
    --color-neutral: #6b7280;
    --color-neutral-50: #f9fafb;
    --color-neutral-100: #f3f4f6;
    --color-neutral-200: #e5e7eb;
    --color-neutral-300: #d1d5db;
    --color-neutral-400: #9ca3af;
    --color-neutral-500: #6b7280;
    --color-neutral-600: #4b5563;
    --color-neutral-700: #374151;
    --color-neutral-800: #1f2937;
    --color-neutral-900: #111827;
    --color-neutral-focus: #4b5563;
    --color-neutral-content: #ffffff;

    /* Info colors */
    --color-info: #3b82f6;
    --color-info-50: #eff6ff;
    --color-info-100: #dbeafe;
    --color-info-200: #bfdbfe;
    --color-info-300: #93c5fd;
    --color-info-400: #60a5fa;
    --color-info-500: #3b82f6;
    --color-info-600: #2563eb;
    --color-info-700: #1d4ed8;
    --color-info-800: #1e40af;
    --color-info-900: #1e3a8a;
    --color-info-focus: #2563eb;
    --color-info-content: #ffffff;

    /* Success colors */
    --color-success: #10b981;
    --color-success-50: #ecfdf5;
    --color-success-100: #d1fae5;
    --color-success-200: #a7f3d0;
    --color-success-300: #6ee7b7;
    --color-success-400: #34d399;
    --color-success-500: #10b981;
    --color-success-600: #059669;
    --color-success-700: #047857;
    --color-success-800: #065f46;
    --color-success-900: #064e3b;
    --color-success-focus: #059669;
    --color-success-content: #ffffff;

    /* Warning colors */
    --color-warning: #f59e0b;
    --color-warning-50: #fffbeb;
    --color-warning-100: #fef3c7;
    --color-warning-200: #fde68a;
    --color-warning-300: #fcd34d;
    --color-warning-400: #fbbf24;
    --color-warning-500: #f59e0b;
    --color-warning-600: #d97706;
    --color-warning-700: #b45309;
    --color-warning-800: #92400e;
    --color-warning-900: #78350f;
    --color-warning-focus: #d97706;
    --color-warning-content: #ffffff;

    /* Error colors */
    --color-error: #ef4444;
    --color-error-50: #fef2f2;
    --color-error-100: #fee2e2;
    --color-error-200: #fecaca;
    --color-error-300: #fca5a5;
    --color-error-400: #f87171;
    --color-error-500: #ef4444;
    --color-error-600: #dc2626;
    --color-error-700: #b91c1c;
    --color-error-800: #991b1b;
    --color-error-900: #7f1d1d;
    --color-error-focus: #dc2626;
    --color-error-content: #ffffff;
}

.dark {
  /* Base colors */
  --color-base: #1f2937;
  --color-base-50: #111827;
  --color-base-100: #1f2937;
  --color-base-200: #374151;
  --color-base-300: #4b5563;
  --color-base-400: #6b7280;
  --color-base-500: #9ca3af;
  --color-base-600: #d1d5db;
  --color-base-700: #e5e7eb;
  --color-base-800: #f3f4f6;
  --color-base-900: #f9fafb;
  --color-base-content: #f9fafb;

  /* Primary colors - Cedar Green (dark mode) */
  --color-primary: #4a8a5e;
  --color-primary-50: #112619;
  --color-primary-100: #183322;
  --color-primary-200: #1f402b;
  --color-primary-300: #264d34;
  --color-primary-400: #2D5A3D;
  --color-primary-500: #4a8a5e;
  --color-primary-600: #8dc3a2;
  --color-primary-700: #b3d7c1;
  --color-primary-800: #d9ebe0;
  --color-primary-900: #f0f7f2;
  --color-primary-focus: #2D5A3D;
  --color-primary-content: #1f2937;
}
</style>
