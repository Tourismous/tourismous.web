<div class="flex flex-col items-center gap-2">

    <div
      class="group relative"
      role="presentation"
    >
      <div class="absolute -inset-1 rounded-xl bg-gradient-to-r from-yellow-300/20 via-yellow-300/40 to-yellow-300/20 blur-lg opacity-75"></div>

      <div class="relative overflow-hidden rounded-xl bg-slate-800 px-8 py-4 cursor-not-allowed">
        <div class="flex items-center gap-4">
          <div class="flex flex-col">
            <span class="text-sm font-medium text-yellow-300/90">Coming in 2025</span>
            <span class="text-lg font-bold text-yellow-300">Join Our Team</span>
          </div>
          <div class="h-8 w-[1px] bg-yellow-300/20"></div>
          <div class="pulse-dot"></div>
          <span class="text-sm text-yellow-300/75">Applications Opening Soon</span>
        </div>

        <div class="absolute inset-0 bg-gradient-to-r from-yellow-300/0 via-yellow-300/5 to-yellow-300/0"></div>

        <div class="absolute inset-0 -translate-x-full animate-shimmer bg-gradient-to-r from-transparent via-yellow-300/10 to-transparent"></div>
      </div>
    </div>

    <button
      class="group flex items-center gap-2 rounded-lg px-4 py-2 text-sm text-slate-400 transition-colors hover:text-yellow-300"
    >
      <span class="text-xs">✉</span>
      <span>Get notified when applications open</span>
    </button>
  </div>

  <style>
    @keyframes shimmer {
      100% { transform: translateX(100%); }
    }

    .animate-shimmer {
      animation: shimmer 3s infinite;
    }

    .pulse-dot {
      @apply h-2 w-2 rounded-full bg-yellow-300;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0% { transform: scale(0.95); opacity: 0.5; }
      50% { transform: scale(1.05); opacity: 0.8; }
      100% { transform: scale(0.95); opacity: 0.5; }
    }
  </style>