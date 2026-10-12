# 📶 ደሴ ማርት (Dessie Mart / ሙጋድ ገበያ) — ይፋዊ የ `offline.html` ፋይል

ለ**ደሴ ማርት (Dessie Mart / ሙጋድ ገበያ)** ተጠቃሚዎች የኢንተርኔት ግንኙነታቸው በሚቋረጥበት ወቅት (Offline Mode) በ **Service Worker (`sw.js`)** አማካኝነት በቀጥታ በስክሪናቸው ላይ የሚታይ 100% የአማርኛ ቋንቋን መሰረት ያደረገ፣ ውብና ደረጃውን የጠበቀ የ **`offline.html`** ገጽ ተዘጋጅቷል።

---

## 🛠️ 1. የፋይሉ አቀማመጥ (File Location)
ይህንን ፋይል ልክ እንደ `manifest.json` እና `sw.js` ሁሉ በድረ-ገጽዎ ዋና ማውጫ (Root / Public Directory) ውስጥ ያስቀምጡት፦
```plaintext
public/offline.html
```

---

## 💻 2. የተሟላ የ `offline.html` ምንጭ ኮድ (Source Code)

```html
<!DOCTYPE html>
<html lang="am" dir="ltr">
<head>
  <meta charset="utf-8"/>
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no"/>
  <title>ደሴ ማርት - የበይነመረብ ግንኙነት ተቋርጧል (Offline)</title>
  <meta name="theme-color" content="#1254d6"/>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Noto+Sans+Ethiopic:wght@400;500;600;700;800&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200" />
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#1254d6',
            'primary-dark': '#0d3fa6',
            secondary: '#f97316',
            'secondary-dark': '#ea580c',
            surface: '#f9f9ff',
            'surface-white': '#ffffff',
            'card-border': '#e2e8f0',
          },
          fontFamily: {
            sans: ['"Noto Sans Ethiopic"', '"Plus Jakarta Sans"', 'sans-serif'],
          }
        }
      }
    }
  </script>
  <style>
    body {
      font-family: 'Noto Sans Ethiopic', 'Plus Jakarta Sans', sans-serif;
      -webkit-tap-highlight-color: transparent;
      user-select: none;
    }
    @keyframes pulse-ring {
      0% { transform: scale(0.95); opacity: 0.8; }
      50% { transform: scale(1.1); opacity: 0.3; }
      100% { transform: scale(0.95); opacity: 0.8; }
    }
    .animate-pulse-ring {
      animation: pulse-ring 3s cubic-bezier(0.4, 0, 0.6, 1) infinite;
    }
  </style>
</head>
<body class="bg-surface text-slate-900 min-h-screen flex flex-col justify-between antialiased selection:bg-primary/20">

  <!-- 🔝 የደሴ ማርት አነስተኛ ራስጌ (Minimal Top Bar) -->
  <header class="w-full bg-surface-white/80 backdrop-blur-md border-b border-card-border/60 py-3.5 px-4 sticky top-0 z-20 flex items-center justify-between">
    <div class="flex items-center gap-2.5">
      <div class="w-8 h-8 rounded-xl bg-primary flex items-center justify-center text-white shadow-sm shadow-primary/30">
        <span class="material-symbols-outlined text-[19px]">storefront</span>
      </div>
      <div>
        <h1 class="text-sm font-bold text-slate-900 leading-tight">ደሴ ማርት</h1>
        <p class="text-[10px] text-slate-500 font-medium leading-none">ሙጋድ ገበያ • Dessie Mart</p>
      </div>
    </div>
    <div class="flex items-center gap-1.5 px-2.5 py-1 rounded-full bg-amber-50 border border-amber-200 text-amber-700 text-[11px] font-semibold">
      <span class="w-2 h-2 rounded-full bg-amber-500 animate-pulse"></span>
      <span>ከመስመር ውጭ (Offline)</span>
    </div>
  </header>

  <!-- 📶 ዋና የይዘት ክፍል (Main Offline State Card) -->
  <main class="flex-1 flex flex-col items-center justify-center px-5 py-8 max-w-md mx-auto w-full text-center">
    
    <!-- ምልክት እና አኒሜሽን (Signal Animated Illustration) -->
    <div class="relative mb-6">
      <div class="w-28 h-28 rounded-full bg-primary/10 flex items-center justify-center animate-pulse-ring absolute inset-0 -m-2"></div>
      <div class="w-24 h-24 rounded-full bg-gradient-to-tr from-primary/15 to-blue-50 border-2 border-primary/20 flex items-center justify-center text-primary relative shadow-md shadow-primary/10">
        <span class="material-symbols-outlined text-4xl">wifi_off</span>
      </div>
      <div class="absolute -bottom-1 -right-1 w-8 h-8 rounded-full bg-secondary text-white flex items-center justify-center shadow-lg border-2 border-white">
        <span class="material-symbols-outlined text-sm">cloud_off</span>
      </div>
    </div>

    <!-- ዋና መልእክት -->
    <h2 class="text-xl font-extrabold text-slate-900 mb-2">
      የበይነመረብ ግንኙነት ተቋርጧል
    </h2>
    <p class="text-sm text-slate-600 mb-6 leading-relaxed px-2">
      ስልክዎ በአሁኑ ወቅት ከኢንተርኔት (ዋይፋይ ወይም የሞባይል ዳታ) ጋር አልተገናኘም። እባክዎ ግንኙነትዎን ፈትሸው በድጋሚ ይሞክሩ።
    </p>

    <!-- ⚡ ፈጣን እርምጃዎች (Quick Action Buttons) -->
    <div class="w-full space-y-3 mb-8">
      <button onclick="window.location.reload()" class="w-full py-3.5 px-5 bg-primary hover:bg-primary-dark active:scale-[0.98] transition-all rounded-2xl text-white font-bold text-sm shadow-lg shadow-primary/25 flex items-center justify-center gap-2">
        <span class="material-symbols-outlined text-lg">refresh</span>
        <span>ድጋሚ ይሞክሩ (Try Again)</span>
      </button>

      <a href="/" class="w-full py-3 px-5 bg-white hover:bg-slate-50 border border-card-border active:scale-[0.98] transition-all rounded-2xl text-slate-700 font-semibold text-xs flex items-center justify-center gap-1.5 shadow-sm">
        <span class="material-symbols-outlined text-base text-slate-500">home</span>
        <span>ወደተቀመጠው መነሻ ገጽ ተመለስ</span>
      </a>
    </div>

    <!-- 💡 ከመስመር ውጭ ምን ማድረግ ይችላሉ? (Offline Capabilities Card) -->
    <div class="w-full bg-white rounded-2xl p-4 border border-card-border shadow-sm text-left">
      <div class="flex items-center gap-2 mb-3">
        <span class="material-symbols-outlined text-primary text-lg">tips_and_updates</span>
        <h3 class="text-xs font-bold text-slate-800 uppercase tracking-wider">የሚመከሩ መፍትሄዎች፦</h3>
      </div>
      <ul class="space-y-2.5 text-xs text-slate-600">
        <li class="flex items-start gap-2">
          <span class="w-1.5 h-1.5 rounded-full bg-primary mt-1.5 flex-shrink-0"></span>
          <span>የስልክዎን ዋይፋይ (Wi-Fi) ወይም የሞባይል ዳታ ክፍት መሆኑን ያረጋግጡ።</span>
        </li>
        <li class="flex items-start gap-2">
          <span class="w-1.5 h-1.5 rounded-full bg-primary mt-1.5 flex-shrink-0"></span>
          <span>ስልክዎን ለ 5 ሰከንድ ወደ <strong>Airplane Mode</strong> ቀይረው መልሰው ይክፈቱት።</span>
        </li>
        <li class="flex items-start gap-2">
          <span class="w-1.5 h-1.5 rounded-full bg-primary mt-1.5 flex-shrink-0"></span>
          <span>አስቀድመው የተመለከቷቸው ገጾች በስልክዎ ካሼ (Cache) ውስጥ ተቀምጠዋል።</span>
        </li>
      </ul>
    </div>

    <!-- 📞 የቀጥታ የስልክ ድጋፍ (Emergency Phone Dial) -->
    <div class="mt-6 flex items-center justify-center gap-2 text-xs text-slate-500">
      <span class="material-symbols-outlined text-sm text-secondary">phone_in_talk</span>
      <span>የደንበኞች ድጋፍ መስመር፦</span>
      <a href="tel:0942188492" class="font-bold text-primary hover:underline">0942 188 492</a>
      <span>ወይም</span>
      <a href="tel:127" class="font-bold text-primary hover:underline">127</a>
    </div>

  </main>

  <!-- 📍 ታችኛው የከተማ መለያ ጽሁፍ -->
  <footer class="w-full py-4 text-center text-[11px] text-slate-400 border-t border-card-border/50">
    <p>ደሴ ማርት (ሙጋድ ገበያ) • በደሴ ከተማ እና በደቡብ ወሎ 🇪🇹</p>
  </footer>

  <script>
    // ኔትወርክ ሲመለስ ገጹ በራስ-ሰር ሪፍሬሽ እንዲሆን ማድረግ (Auto-reload on online)
    window.addEventListener('online', () => {
      window.location.reload();
    });
  </script>
</body>
</html>
```

---

## 🌟 በስክሪኑ ውስጥ የተካተቱ ቁልፍ ባህሪያት፦
1. **አውቶሜትድ ኔትወርክ ሪሎድ (Auto-Reload on Online):** ተጠቃሚው የሞባይል ዳታውን ወይም ዋይፋዩን ሲያበራ ገጹ በራሱ ሰከንድ ሳይቆይ ሪፍሬሽ ያደርጋል።
2. **ድጋሚ መሞከሪያ (Refresh Button):** በቀላሉ በ 1 ንክኪ ኔትወርክን ለመፈተሽ የሚያስችል ጎላ ያለ የሮያል ሰማያዊ አዝራር።
3. **የቀጥታ ስልክ ጥሪ (Direct Click-to-Call):** ኢንተርኔት ባይኖርም ተጠቃሚዎች የደሴ ማርትን የስልክ ድጋፍ ቁጥሮች (`127` እና `0942188492`) በቀጥታ እንዲደውሉ ያስችላል።
4. **ንጹህ ዲዛይንና ቀለማት:** ከደሴ ማርት ይፋዊ ብራንድ ቀለማት (`#1254d6` እና `#f97316`) ጋር 100% የተጣጣመ።
