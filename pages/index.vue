<template>
  <main>
    <header
      class="fixed top-0 left-0 w-full z-50 border-b backdrop-blur bg-background/80"
    >
      <div class="container flex h-16 items-center justify-between px-4">
        <div class="flex items-center gap-6">
          <a aria-label="Homepage" class="flex items-center gap-2" href="/">
            <img src="/cedar-logo.png" alt="Cedar Devs" class="h-8" />
            <span class="text-xl font-bold text-foreground">Cedar Devs</span>
          </a>
          <nav class="hidden md:flex items-center gap-6">
            <a
              class="text-sm font-medium text-foreground hover:text-primary transition"
              href="#why-us"
              >Why Us</a
            >
            <a
              class="text-sm font-medium text-foreground hover:text-primary transition"
              href="#pricing"
              >Pricing</a
            >
            <a
              class="text-sm font-medium text-foreground hover:text-primary transition"
              href="#how-it-works"
              >How It Works</a
            >
            <a
              class="text-sm font-medium text-foreground hover:text-primary transition"
              href="#contact"
              >Contact</a
            >
          </nav>
        </div>
        <div class="hidden md:flex items-center gap-4">
          <a
            class="inline-flex items-center justify-center whitespace-nowrap transition-colors focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 bg-primary text-primary-content shadow-sm hover:bg-primary-focus h-10 px-6 rounded-full text-sm font-semibold"
            href="#contact"
            >Get Started</a
          >
        </div>
        <!-- Mobile Menu Button -->
        <button
          class="p-2 md:hidden"
          aria-label="Toggle menu"
          @click="mobileMenuOpen = !mobileMenuOpen"
        >
          <svg
            v-if="!mobileMenuOpen"
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path d="M3 12h18"></path>
            <path d="M3 18h18"></path>
            <path d="M3 6h18"></path>
          </svg>
          <svg
            v-else
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <path d="M18 6L6 18"></path>
            <path d="M6 6l12 12"></path>
          </svg>
        </button>
      </div>
      <!-- Mobile Menu -->
      <div
        v-if="mobileMenuOpen"
        class="md:hidden bg-background border-t border-base-200"
      >
        <nav class="flex flex-col p-4 gap-4">
          <a
            class="text-sm font-medium text-foreground hover:text-primary transition py-2"
            href="#why-us"
            @click="mobileMenuOpen = false"
            >Why Us</a
          >
          <a
            class="text-sm font-medium text-foreground hover:text-primary transition py-2"
            href="#pricing"
            @click="mobileMenuOpen = false"
            >Pricing</a
          >
          <a
            class="text-sm font-medium text-foreground hover:text-primary transition py-2"
            href="#how-it-works"
            @click="mobileMenuOpen = false"
            >How It Works</a
          >
          <a
            class="text-sm font-medium text-foreground hover:text-primary transition py-2"
            href="#contact"
            @click="mobileMenuOpen = false"
            >Contact</a
          >
          <a
            class="inline-flex items-center justify-center bg-primary text-primary-content shadow-sm hover:bg-primary-focus h-10 px-6 rounded-full text-sm font-semibold mt-2"
            href="#contact"
            @click="mobileMenuOpen = false"
            >Get Started</a
          >
        </nav>
      </div>
    </header>
    <main class="min-h-[calc(100vh-176px)] bg-background">
      <section id="hero" class="flex flex-col">
        <div
          class="flex flex-col items-center pt-24 sm:pt-28 md:pt-32 lg:pt-40 pb-16 sm:pb-20 md:pb-24"
        >
          <div
            class="flex w-full max-w-5xl flex-col space-y-6 overflow-hidden pt-8 px-4"
          >
            <h1
              class="text-center text-foreground font-semibold tracking-[-0.02em] text-[2.25rem] sm:text-[3rem] md:text-[3.5rem] lg:text-[4rem] leading-tight"
              style="filter: blur(0px); opacity: 1; transform: none"
            >
              <span class="inline" style="opacity: 1; transform: none"
                >Hire Talented, </span
              ><span class="inline" style="opacity: 1; transform: none"
                >Full Time Developers</span
              ><span class="inline" style="opacity: 1; transform: none">
                starting at <span class="text-primary">$8/hr</span></span
              >
            </h1>
          </div>
          <div
            class="mx-auto mt-6 flex w-full max-w-2xl flex-col items-center justify-center space-y-4 sm:flex-row sm:space-x-4 sm:space-y-0"
            style="opacity: 1; transform: none"
          >
            <div class="flex flex-col items-center gap-4">
              <div
                class="flex flex-col sm:flex-row gap-3 justify-center w-full sm:w-auto"
              >
                <a
                  class="inline-flex items-center justify-center whitespace-nowrap text-sm font-medium focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 shadow h-10 rounded-full px-6 relative overflow-hidden group transition-all duration-300 bg-secondary hover:bg-secondary/90 text-secondary-foreground"
                  href="#contact"
                  ><span class="relative z-10 flex items-center font-medium"
                    >Get Started</span
                  ><span
                    class="absolute inset-0 bg-gradient-to-r from-primary-light to-primary opacity-0 group-hover:opacity-100 transition-opacity duration-300"
                  ></span
                ></a>
              </div>
              <a
                class="flex items-center gap-1 text-sm font-medium py-1 relative group transition-all duration-300 text-muted-foreground hover:text-foreground"
                href="#contact"
                ><span>Need help? Book a call</span
                ><span
                  class="absolute bottom-0 left-0 right-0 h-px bg-current transform scale-x-0 group-hover:scale-x-100 transition-transform duration-300 origin-left"
                ></span
              ></a>
            </div>
          </div>
        </div>
      </section>

      <!-- Quality Over Price Section -->
      <section id="why-us" class="py-20 bg-base-50">
        <div class="container mx-auto px-4">
          <div class="max-w-4xl mx-auto text-center">
            <div
              class="inline-flex items-center justify-center w-16 h-16 rounded-full bg-primary/10 mb-6"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-8 h-8 text-primary"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"
                />
              </svg>
            </div>
            <h2
              class="text-3xl sm:text-4xl md:text-5xl font-bold text-foreground mb-6"
            >
              Not Cheap Developers.<br />
              <span class="text-primary">Exceptional Talent</span> at Fair
              Rates.
            </h2>
            <p
              class="text-lg sm:text-xl text-muted-foreground mb-10 max-w-3xl mx-auto leading-relaxed"
            >
              Our developers come from
              <span class="text-foreground font-semibold">Lebanon</span>, home
              to world-class accredited universities like the American
              University of Beirut and Lebanese American University. We don't
              just interview them —
              <span class="text-foreground font-semibold"
                >we build real projects together</span
              >. That's how we know they're exceptional.
            </p>

            <div class="grid md:grid-cols-3 gap-8 mt-12">
              <div
                class="bg-background rounded-2xl p-8 shadow-sm border border-base-200"
              >
                <div
                  class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center mx-auto mb-4"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="w-6 h-6 text-primary"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M12 14l9-5-9-5-9 5 9 5z"
                    />
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"
                    />
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M12 14l9-5-9-5-9 5 9 5zm0 0l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14zm-4 6v-7.5l4-2.222"
                    />
                  </svg>
                </div>
                <h3 class="text-xl font-semibold text-foreground mb-3">
                  Top-Tier Education
                </h3>
                <p class="text-muted-foreground">
                  Graduates from Lebanon's internationally accredited
                  universities, trained in rigorous computer science and
                  engineering programs.
                </p>
              </div>

              <div
                class="bg-background rounded-2xl p-8 shadow-sm border border-base-200"
              >
                <div
                  class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center mx-auto mb-4"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="w-6 h-6 text-primary"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"
                    />
                  </svg>
                </div>
                <h3 class="text-xl font-semibold text-foreground mb-3">
                  Battle-Tested Skills
                </h3>
                <p class="text-muted-foreground">
                  We work alongside every developer on real projects before they
                  join. No guesswork — we've seen their code in action.
                </p>
              </div>

              <div
                class="bg-background rounded-2xl p-8 shadow-sm border border-base-200"
              >
                <div
                  class="w-12 h-12 rounded-full bg-primary/10 flex items-center justify-center mx-auto mb-4"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="w-6 h-6 text-primary"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="2"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
                    />
                  </svg>
                </div>
                <h3 class="text-xl font-semibold text-foreground mb-3">
                  Fair Rates, Not Cheap
                </h3>
                <p class="text-muted-foreground">
                  Lebanon's cost of living means our developers earn well
                  locally while offering you exceptional value. Everyone wins.
                </p>
              </div>
            </div>

            <div
              class="mt-12 p-6 bg-primary/5 rounded-2xl border border-primary/20"
            >
              <p class="text-foreground font-medium text-lg">
                "The best investment isn't always the cheapest or the most
                expensive — it's the one that delivers the most value."
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- Pricing Comparison Section -->
      <section id="pricing" class="py-20 bg-background">
        <div class="container mx-auto px-4">
          <div class="max-w-5xl mx-auto">
            <div class="text-center mb-12">
              <h2
                class="text-3xl sm:text-4xl md:text-5xl font-bold text-foreground mb-4"
              >
                Best Value in the Market
              </h2>
              <p class="text-lg text-muted-foreground max-w-2xl mx-auto">
                Don't overpay for the logo. Hire the talent.
              </p>
            </div>

            <!-- Pricing Comparison - Matching Reference Design -->
            <div class="flex flex-col md:flex-row gap-6 md:gap-0 items-start">
              <!-- Experience Labels (Left Side) -->
              <div
                class="hidden md:flex flex-col justify-start pt-24 pr-8 w-56 shrink-0"
              >
                <!-- 0-2 Years -->
                <div class="h-24 flex flex-col justify-center">
                  <div class="text-sm text-muted-foreground">
                    Full-Time Developer
                  </div>
                  <div class="font-semibold text-foreground">
                    0-2 Years of Experience
                  </div>
                </div>
                <!-- 2-5 Years -->
                <div class="h-24 flex flex-col justify-center">
                  <div class="text-sm text-muted-foreground">
                    Full-Time Developer
                  </div>
                  <div class="font-semibold text-foreground">
                    2-5 Years of Experience
                  </div>
                </div>
                <!-- 5+ Years -->
                <div class="h-24 flex flex-col justify-center">
                  <div class="text-sm text-muted-foreground">
                    Full-Time Developer
                  </div>
                  <div class="font-semibold text-foreground">
                    5+ Years of Experience
                  </div>
                </div>
              </div>

              <!-- Company Cards -->
              <div class="flex flex-col md:flex-row gap-4 flex-1">
                <!-- Cedar Devs Card -->
                <div
                  class="flex-1 rounded-2xl border-2 border-primary/30 bg-primary/5 overflow-hidden"
                >
                  <!-- Logo Header -->
                  <div
                    class="p-6 flex items-center justify-center gap-2 border-b border-primary/20"
                  >
                    <img src="/cedar-logo.png" alt="Cedar Devs" class="h-8" />
                    <span class="font-semibold text-foreground"
                      >Cedar Devs</span
                    >
                  </div>
                  <!-- Prices -->
                  <div class="flex flex-col">
                    <div
                      class="h-24 flex flex-col items-center justify-center border-b border-primary/20"
                    >
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        0-2 Years
                      </div>
                      <div class="text-2xl font-bold text-primary">
                        $1,500<span class="text-base font-normal">/mo</span>
                      </div>
                    </div>
                    <div
                      class="h-24 flex flex-col items-center justify-center border-b border-primary/20"
                    >
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        2-5 Years
                      </div>
                      <div class="text-2xl font-bold text-primary">
                        $3,000<span class="text-base font-normal">/mo</span>
                      </div>
                    </div>
                    <div class="h-24 flex flex-col items-center justify-center">
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        5+ Years
                      </div>
                      <div class="text-2xl font-bold text-primary">
                        $4,000<span class="text-base font-normal">/mo</span>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- Upwork Card -->
                <div
                  class="flex-1 rounded-2xl border border-base-200 bg-background overflow-hidden"
                >
                  <!-- Logo Header -->
                  <div
                    class="p-6 flex items-center justify-center border-b border-base-200 h-[76px]"
                  >
                    <img
                      src="/upwork-logo.webp"
                      alt="Upwork"
                      class="h-8 object-contain"
                    />
                  </div>
                  <!-- Prices -->
                  <div class="flex flex-col">
                    <div
                      class="h-24 flex flex-col items-center justify-center border-b border-base-100"
                    >
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        0-2 Years
                      </div>
                      <div class="text-2xl font-semibold text-foreground">
                        $2,400<span
                          class="text-base font-normal text-muted-foreground"
                          >/mo</span
                        >
                      </div>
                      <div class="text-sm text-muted-foreground">(-$900)</div>
                    </div>
                    <div
                      class="h-24 flex flex-col items-center justify-center border-b border-base-100"
                    >
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        2-5 Years
                      </div>
                      <div class="text-2xl font-semibold text-foreground">
                        $4,000<span
                          class="text-base font-normal text-muted-foreground"
                          >/mo</span
                        >
                      </div>
                      <div class="text-sm text-muted-foreground">(-$1,000)</div>
                    </div>
                    <div class="h-24 flex flex-col items-center justify-center">
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        5+ Years
                      </div>
                      <div class="text-2xl font-semibold text-foreground">
                        $5,600<span
                          class="text-base font-normal text-muted-foreground"
                          >/mo</span
                        >
                      </div>
                      <div class="text-sm text-muted-foreground">(-$1,600)</div>
                    </div>
                  </div>
                </div>

                <!-- Toptal Card -->
                <div
                  class="flex-1 rounded-2xl border border-base-200 bg-background overflow-hidden"
                >
                  <!-- Logo Header -->
                  <div
                    class="p-6 flex items-center justify-center border-b border-base-200 h-[76px]"
                  >
                    <img
                      src="/toptal-logo.webp"
                      alt="Toptal"
                      class="h-8 object-contain"
                    />
                  </div>
                  <!-- Prices -->
                  <div class="flex flex-col">
                    <div
                      class="h-24 flex flex-col items-center justify-center border-b border-base-100"
                    >
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        0-2 Years
                      </div>
                      <div class="text-2xl font-semibold text-foreground">
                        $3,200<span
                          class="text-base font-normal text-muted-foreground"
                          >/mo</span
                        >
                      </div>
                      <div class="text-sm text-muted-foreground">(-$1,700)</div>
                    </div>
                    <div
                      class="h-24 flex flex-col items-center justify-center border-b border-base-100"
                    >
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        2-5 Years
                      </div>
                      <div class="text-2xl font-semibold text-foreground">
                        $5,200<span
                          class="text-base font-normal text-muted-foreground"
                          >/mo</span
                        >
                      </div>
                      <div class="text-sm text-muted-foreground">(-$2,200)</div>
                    </div>
                    <div class="h-24 flex flex-col items-center justify-center">
                      <div class="md:hidden text-xs text-muted-foreground mb-1">
                        5+ Years
                      </div>
                      <div class="text-2xl font-semibold text-foreground">
                        $8,200<span
                          class="text-base font-normal text-muted-foreground"
                          >/mo</span
                        >
                      </div>
                      <div class="text-sm text-muted-foreground">(-$4,200)</div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <!-- CTA -->
            <div class="text-center mt-12">
              <a
                href="#contact"
                class="inline-flex items-center justify-center px-8 py-3 rounded-full bg-primary text-primary-content font-semibold hover:bg-primary-focus transition-colors"
              >
                Start Saving Today
              </a>
            </div>
          </div>
        </div>
      </section>

      <!-- How It Works Section -->
      <section id="how-it-works" class="py-20 bg-base-50">
        <div class="container mx-auto px-4">
          <div class="max-w-5xl mx-auto">
            <div class="text-center mb-16">
              <h2
                class="text-3xl sm:text-4xl md:text-5xl font-bold text-foreground mb-4"
              >
                Simple as 1, 2, 3
              </h2>
              <p class="text-lg text-muted-foreground max-w-2xl mx-auto">
                Getting started with Cedar Devs is easy. Here's how it works.
              </p>
            </div>

            <div class="grid md:grid-cols-3 gap-8 md:gap-12">
              <!-- Step 1 -->
              <div class="relative text-center">
                <div
                  class="w-16 h-16 rounded-full bg-primary text-primary-content text-2xl font-bold flex items-center justify-center mx-auto mb-6"
                >
                  1
                </div>
                <div
                  class="hidden md:block absolute top-8 left-[60%] w-[80%] h-0.5 bg-primary/20"
                ></div>
                <div
                  class="w-20 h-20 rounded-2xl bg-primary/10 flex items-center justify-center mx-auto mb-6"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="w-10 h-10 text-primary"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="1.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"
                    />
                  </svg>
                </div>
                <h3 class="text-xl font-semibold text-foreground mb-3">
                  Tell Us Your Needs
                </h3>
                <p class="text-muted-foreground">
                  Schedule a quick call with us to discuss your project
                  requirements, tech stack, and the type of developer you're
                  looking for.
                </p>
              </div>

              <!-- Step 2 -->
              <div class="relative text-center">
                <div
                  class="w-16 h-16 rounded-full bg-primary text-primary-content text-2xl font-bold flex items-center justify-center mx-auto mb-6"
                >
                  2
                </div>
                <div
                  class="hidden md:block absolute top-8 left-[60%] w-[80%] h-0.5 bg-primary/20"
                ></div>
                <div
                  class="w-20 h-20 rounded-2xl bg-primary/10 flex items-center justify-center mx-auto mb-6"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="w-10 h-10 text-primary"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="1.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"
                    />
                  </svg>
                </div>
                <h3 class="text-xl font-semibold text-foreground mb-3">
                  We Match You
                </h3>
                <p class="text-muted-foreground">
                  We hand-pick developers from our vetted talent pool that
                  perfectly match your requirements and company culture.
                </p>
              </div>

              <!-- Step 3 -->
              <div class="relative text-center">
                <div
                  class="w-16 h-16 rounded-full bg-primary text-primary-content text-2xl font-bold flex items-center justify-center mx-auto mb-6"
                >
                  3
                </div>
                <div
                  class="w-20 h-20 rounded-2xl bg-primary/10 flex items-center justify-center mx-auto mb-6"
                >
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="w-10 h-10 text-primary"
                    fill="none"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                    stroke-width="1.5"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      d="M14.25 9.75L16.5 12l-2.25 2.25m-4.5 0L7.5 12l2.25-2.25M6 20.25h12A2.25 2.25 0 0020.25 18V6A2.25 2.25 0 0018 3.75H6A2.25 2.25 0 003.75 6v12A2.25 2.25 0 006 20.25z"
                    />
                  </svg>
                </div>
                <h3 class="text-xl font-semibold text-foreground mb-3">
                  Start Building
                </h3>
                <p class="text-muted-foreground">
                  Your new developer joins your team and starts contributing
                  immediately. It's that simple.
                </p>
              </div>
            </div>

            <!-- CTA -->
            <div class="text-center mt-16">
              <a
                href="/get-started"
                class="inline-flex items-center justify-center px-8 py-3 rounded-full bg-secondary text-secondary-content font-semibold hover:bg-secondary-focus transition-colors"
              >
                Get Started Now
              </a>
            </div>
          </div>
        </div>
      </section>
      <section
        id="contact"
        class="py-24 bg-gradient-to-br from-primary-50 via-white to-secondary-50 relative overflow-hidden"
      >
        <!-- Background decorations -->
        <div
          class="absolute top-0 right-0 w-96 h-96 bg-primary-200/30 rounded-full blur-3xl"
        ></div>
        <div
          class="absolute bottom-0 left-0 w-80 h-80 bg-secondary-200/30 rounded-full blur-3xl"
        ></div>
        <div class="container mx-auto px-4 relative z-10">
          <div class="text-center mb-12">
            <span
              class="inline-block px-4 py-1 bg-primary-100 text-primary-700 rounded-full text-sm font-medium mb-4"
              >Contact Us</span
            >
            <h2 class="text-4xl font-bold text-foreground mb-4">
              Get in Touch
            </h2>
            <p class="text-lg text-muted-foreground max-w-2xl mx-auto">
              Ready to hire exceptional developers from Lebanon? Contact us
              today and let's build something great together.
            </p>
          </div>
          <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 max-w-6xl mx-auto">
            <div class="flex flex-col justify-center">
              <div class="space-y-6">
                <div
                  class="flex items-center bg-background p-5 rounded-2xl shadow-sm border border-base-200 hover:shadow-md transition-all duration-300"
                >
                  <div
                    class="w-14 h-14 bg-primary rounded-xl flex items-center justify-center mr-4"
                  >
                    <i class="fa-solid fa-envelope text-white text-xl"></i>
                  </div>
                  <div>
                    <h4 class="font-semibold text-foreground">Email Us</h4>
                    <p class="text-primary">afawaz@cedardevs.com</p>
                  </div>
                </div>

                <div
                  class="flex items-center bg-background p-5 rounded-2xl shadow-sm border border-base-200 hover:shadow-md transition-all duration-300"
                >
                  <div
                    class="w-14 h-14 bg-secondary rounded-xl flex items-center justify-center mr-4"
                  >
                    <i class="fa-solid fa-calendar text-white text-xl"></i>
                  </div>
                  <div>
                    <h4 class="font-semibold text-foreground">
                      Schedule a Call
                    </h4>
                    <p class="text-muted-foreground">
                      Book a free consultation
                    </p>
                  </div>
                </div>
              </div>
              <div class="mt-8">
                <p class="mb-4 text-muted-foreground font-medium">
                  Follow us on social media
                </p>
                <div class="flex space-x-3">
                  <a
                    href="https://www.linkedin.com/company/cedar-devs"
                    class="w-12 h-12 bg-primary rounded-xl flex items-center justify-center text-white hover:bg-primary-focus cursor-pointer transition-all duration-300"
                  >
                    <i class="fa-brands fa-linkedin-in text-lg"></i>
                  </a>
                  <a
                    href="#"
                    class="w-12 h-12 bg-primary rounded-xl flex items-center justify-center text-white hover:bg-primary-focus cursor-pointer transition-all duration-300"
                  >
                    <i class="fa-brands fa-twitter text-lg"></i>
                  </a>
                  <a
                    href="#"
                    class="w-12 h-12 bg-secondary rounded-xl flex items-center justify-center text-white hover:bg-secondary-focus cursor-pointer transition-all duration-300"
                  >
                    <i class="fa-brands fa-github text-lg"></i>
                  </a>
                </div>
              </div>
            </div>
            <div>
              <div
                class="bg-background p-8 rounded-2xl shadow-xl border border-base-200"
              >
                <h3 class="text-2xl font-semibold mb-6 text-foreground">
                  Send Us a Message
                </h3>
                <form @submit.prevent="handleSubmit" class="space-y-4">
                  <div class="mb-4">
                    <label
                      class="block text-sm font-medium text-foreground mb-2"
                      for="name"
                      >Full Name</label
                    >
                    <input
                      id="name"
                      type="text"
                      v-model="form.name"
                      class="w-full p-4 border border-base-200 rounded-xl focus:ring-2 focus:ring-primary focus:border-primary transition-all duration-300"
                      placeholder="Your name"
                      required
                    />
                  </div>
                  <div class="mb-4">
                    <label
                      class="block text-sm font-medium text-foreground mb-2"
                      for="email"
                      >Email Address</label
                    >
                    <input
                      id="email"
                      type="email"
                      v-model="form.email"
                      class="w-full p-4 border border-base-200 rounded-xl focus:ring-2 focus:ring-primary focus:border-primary transition-all duration-300"
                      placeholder="your@email.com"
                      required
                    />
                  </div>
                  <div class="mb-4">
                    <label
                      class="block text-sm font-medium text-foreground mb-2"
                      for="company"
                      >Company</label
                    >
                    <input
                      id="company"
                      type="text"
                      v-model="form.company"
                      class="w-full p-4 border border-base-200 rounded-xl focus:ring-2 focus:ring-primary focus:border-primary transition-all duration-300"
                      placeholder="Your company name"
                    />
                  </div>
                  <div class="mb-4">
                    <label
                      class="block text-sm font-medium text-foreground mb-2"
                      for="message"
                      >Message</label
                    >
                    <textarea
                      id="message"
                      rows="4"
                      v-model="form.message"
                      class="w-full p-4 border border-base-200 rounded-xl focus:ring-2 focus:ring-primary focus:border-primary transition-all duration-300"
                      placeholder="Tell us about your project"
                      required
                    ></textarea>
                  </div>

                  <div
                    v-if="submitStatus.message"
                    :class="{
                      'text-success bg-success/10 p-3 rounded-lg':
                        submitStatus.success,
                      'text-error bg-error/10 p-3 rounded-lg':
                        !submitStatus.success,
                    }"
                    class="mb-4"
                  >
                    {{ submitStatus.message }}
                  </div>
                  <button
                    type="submit"
                    class="w-full bg-primary hover:bg-primary-focus text-primary-content py-4 px-6 rounded-xl transition-all duration-300 font-semibold shadow-lg hover:shadow-xl"
                    :disabled="isSubmitting"
                  >
                    {{ isSubmitting ? "Sending..." : "Send Message" }}
                    <i class="fa-solid fa-paper-plane ml-2"></i>
                  </button>
                </form>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Footer -->
      <footer class="bg-primary-900 text-primary-100 py-16">
        <div class="container mx-auto px-4">
          <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
            <!-- Logo and Description -->
            <div class="md:col-span-2">
              <div class="flex items-center gap-3 mb-4">
                <img src="/cedar-logo.png" alt="Cedar Devs" class="h-12" />
                <span class="text-xl font-bold text-white">Cedar Devs</span>
              </div>
              <p class="text-sm text-primary-200 leading-relaxed max-w-md">
                Connecting you with exceptional software developers from
                Lebanon. Quality talent, fair rates, real results.
              </p>
            </div>

            <!-- Quick Links -->
            <div>
              <h4 class="text-white font-semibold mb-4">Quick Links</h4>
              <ul class="space-y-2">
                <li>
                  <a
                    href="#why-us"
                    class="text-primary-200 hover:text-white transition"
                    >Why Us</a
                  >
                </li>
                <li>
                  <a
                    href="#pricing"
                    class="text-primary-200 hover:text-white transition"
                    >Pricing</a
                  >
                </li>
                <li>
                  <a
                    href="#how-it-works"
                    class="text-primary-200 hover:text-white transition"
                    >How It Works</a
                  >
                </li>
                <li>
                  <a
                    href="#contact"
                    class="text-primary-200 hover:text-white transition"
                    >Contact</a
                  >
                </li>
              </ul>
            </div>

            <!-- Contact Info -->
            <div>
              <h4 class="text-white font-semibold mb-4">Contact</h4>
              <ul class="space-y-2">
                <li class="text-primary-200">
                  <i class="fa-solid fa-envelope mr-2"></i>
                  afawaz@cedardevs.com
                </li>
                <li class="text-primary-200">
                  <i class="fa-solid fa-location-dot mr-2"></i>
                  Lebanon
                </li>
              </ul>
            </div>
          </div>

          <div class="border-t border-primary-700 mt-12 pt-8">
            <div class="flex flex-col md:flex-row justify-between items-center">
              <p class="text-sm mb-4 md:mb-0 text-primary-300">
                © 2024 Cedar Devs. All rights reserved.
              </p>
              <div class="flex space-x-4">
                <a
                  href="#"
                  class="w-10 h-10 bg-primary-800 hover:bg-primary rounded-lg flex items-center justify-center transition-all duration-300"
                  ><i
                    class="fab fa-twitter text-primary-200 hover:text-white"
                  ></i
                ></a>
                <a
                  href="https://www.linkedin.com/company/cedar-devs"
                  class="w-10 h-10 bg-primary-800 hover:bg-primary rounded-lg flex items-center justify-center transition-all duration-300"
                  ><i
                    class="fab fa-linkedin text-primary-200 hover:text-white"
                  ></i
                ></a>
                <a
                  href="#"
                  class="w-10 h-10 bg-primary-800 hover:bg-primary rounded-lg flex items-center justify-center transition-all duration-300"
                  ><i
                    class="fab fa-github text-primary-200 hover:text-white"
                  ></i
                ></a>
              </div>
            </div>
          </div>
        </div>
      </footer>
    </main>
  </main>
</template>

<script setup>
import { ref, onMounted } from "vue";

const isDark = ref(false);
const mobileMenuOpen = ref(false);
const form = ref({
  name: "",
  email: "",
  company: "",
  message: "",
});

const isSubmitting = ref(false);
const submitStatus = ref({
  success: false,
  message: "",
});

const videoPlayer = ref(null);
const videoPlaceholder = ref(null);
const isVideoPlaying = ref(false);

const playVideo = () => {
  if (videoPlayer.value) {
    if (videoPlayer.value.paused) {
      videoPlayer.value.play();
      isVideoPlaying.value = true;
    } else {
      videoPlayer.value.pause();
      isVideoPlaying.value = false;
    }
  }
};

const toggleDarkMode = () => {
  isDark.value = !isDark.value;
  document.documentElement.classList.toggle("dark");
};

const handleSubmit = async () => {
  try {
    isSubmitting.value = true;
    submitStatus.value = { success: false, message: "" };

    // Validate form
    if (!form.value.name || !form.value.email || !form.value.message) {
      throw new Error("Please fill in all required fields");
    }

    // Send form data to API
    const response = await $fetch("/api/contact", {
      method: "POST",
      body: { ...form.value, source: "cedardevs" },
    });

    if (response.status === 200) {
      submitStatus.value = {
        success: true,
        message: "Thank you for your message! We will get back to you soon.",
      };
      // Reset form
      form.value = {
        name: "",
        email: "",
        company: "",
        message: "",
      };
    } else {
      throw new Error(response.message || "Failed to send message");
    }
  } catch (error) {
    submitStatus.value = {
      success: false,
      message: error.message || "Something went wrong. Please try again.",
    };
  } finally {
    isSubmitting.value = false;
  }
};

// Video player functionality
onMounted(() => {
  // Mobile Menu Toggle (if needed in the future)
  // const mobileMenuButton = document.getElementById("mobile-menu-button");
  // const mobileMenu = document.getElementById("mobile-menu");

  // Sticky Header
  const header = document.getElementById("header");

  window.addEventListener("scroll", () => {
    if (window.scrollY > 100) {
      header.classList.add("py-2");
      header.classList.add("shadow-md");
    } else {
      header.classList.remove("py-2");
      header.classList.remove("shadow-md");
    }
  });

  // Smooth Scrolling for Navigation Links
  document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
    anchor.addEventListener("click", function (e) {
      e.preventDefault();

      const target = document.querySelector(this.getAttribute("href"));
      if (target) {
        window.scrollTo({
          top: target.offsetTop - 80,
          behavior: "smooth",
        });
      }
    });
  });
});
// Mobile Menu Toggle
</script>

<style scoped>
/* Hero Animation Keyframes */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInRight {
  from {
    opacity: 0;
    transform: translateX(30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
body {
  font-family: "Nunito", sans-serif;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes floatUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Hero Section Animations */
.hero-title {
  animation: fadeInUp 0.8s ease-out 0.2s both;
}

.hero-subtitle {
  animation: fadeInUp 0.8s ease-out 0.4s both;
}

.hero-buttons {
  animation: fadeInUp 0.8s ease-out 0.6s both;
}

.hero-stats {
  animation: fadeInUp 0.8s ease-out 0.8s both;
}

.hero-visual {
  animation: fadeInRight 0.8s ease-out 0.3s both;
}

.hero-main-card {
  animation: fadeIn 1s ease-out 0.5s both;
}

.hero-floating-card-1 {
  animation: floatUp 0.8s ease-out 0.9s both;
}

.hero-floating-card-2 {
  animation: floatUp 0.8s ease-out 1.1s both;
}

/* Add subtle hover effects */
.hero-buttons a,
.hero-buttons button {
  transition: all 0.3s ease;
}

.hero-buttons a:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.hero-buttons button:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.hero-floating-card-1,
.hero-floating-card-2 {
  transition: transform 0.3s ease;
}

.hero-floating-card-1:hover,
.hero-floating-card-2:hover {
  transform: translateY(-3px);
}

/* Responsive adjustments */
@media (max-width: 1024px) {
  .hero-visual {
    animation: fadeInUp 0.8s ease-out 0.7s both;
  }
}
</style>
