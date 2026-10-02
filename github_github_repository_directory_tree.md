# 🐙 ደሴ ማርት (Dessie Mart / ሙጋድ ገበያ) — የተሟላ የ GitHub ሪፖዚቶሪ ፎልደር መዋቅር (Repository Directory Tree & Architecture)

---

## 📌 1. የ GitHub ፕሮጀክት አጠቃላይ መዋቅር (Project Architecture Overview)
ይህ የሪፖዚቶሪ መዋቅር ለ**ደሴ ማርት (Dessie Mart / ሙጋድ ገበያ)** ኢንጂነሪንግ ቡድን የተዘጋጀ ሲሆን፣ ሁለቱንም የሞባይል አፕሊኬሽን (Flutter Frontend)፣ የባክ-ኤንድ ሰርቨር (Node.js/Express API + Webhooks)፣ እና አውቶሜትድ የ CI/CD ፓይፕላይኖችን በአንድ ወጥ የሞኖሪፖ/ባለብዙ ሞጁል (Clean Architecture) ቅርጸት ያደራጃል።

---

## 📂 2. የፋይሎችና የፎልደሮች የተሟላ ዝርዝር ዛፍ (Complete Repository Directory Tree)

```plaintext
dessie-mart/
│
├── .github/                                # 🤖 GitHub Actions & Workflows
│   ├── workflows/
│   │   ├── build_android.yml               # አውቶሜትድ APK እና AAB ግንባታ ፓይፕላይን
│   │   ├── build_ios.yml                   # iOS IPA እና TestFlight ማሰማሪያ
│   │   ├── deploy_backend.yml              # የባክ-ኤንድ ሰርቨር ወደ Cloud ማሰማሪያ
│   │   └── run_tests.yml                   # ዩኒት እና የሳንድቦክስ ኤፒአይ ቴስቶች
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md                   # የስህተት ጥቆማ ፎርም
│   │   └── feature_request.md              # አዳዲስ ተጨማሪ አገልግሎቶች መጠየቂያ
│   └── PULL_REQUEST_TEMPLATE.md            # ለኮድ ክለሳ (PR) የሚሆን መመሪያ
│
├── android/                                # 📱 Android Native Configuration
│   ├── app/
│   │   ├── build.gradle                    # Application ID (com.dessiemart.app), SDK 34, ProGuard
│   │   ├── proguard-rules.pro              # የቴሌብር/ሲቢኢ ሞዴሎችና የአማርኛ ፊደላት ጥበቃ
│   │   └── src/main/
│   │       ├── AndroidManifest.xml         # የስልክ ፍቃዶች (Camera, Internet, Storage)
│   │       └── res/                        # የመተግበሪያ አዶዎች (mipmap/ic_launcher - Squircle)
│   ├── key.properties.example              # የምስክር ወረቀት (Keystore) ማዋቀሪያ ናሙና
│   ├── build.gradle
│   └── settings.gradle
│
├── ios/                                    # 🍏 iOS Native Configuration
│   ├── Runner/
│   │   ├── Info.plist                      # የካሜራ፣ ማይክራፎን እና ስልክ ጥሪ ፈቃዶች
│   │   └── Assets.xcassets/                # iOS App Icon እና ስፕላሽ ምስሎች
│   └── Podfile
│
├── lib/                                    # 💙 Flutter Mobile Frontend Code (Clean Architecture)
│   ├── main.dart                           # የመተግበሪያው መነሻ (Entry Point & Theme Setup)
│   ├── core/
│   │   ├── constants/
│   │   │   ├── api_endpoints.dart          # የቴሌብር፣ ሲቢኢ እና የደሴ ማርት ኤፒአይ አድራሻዎች
│   │   │   └── app_strings_am.dart         # የአማርኛ ጽሁፎች፣ ቃላት እና መለያዎች
│   │   ├── theme/
│   │   │   ├── app_colors.dart             # ሮያል ሰማያዊ (#1254d6) እና ብርቱካናማ (#f97316)
│   │   │   └── app_typography.dart         # Noto Sans Ethiopic / Plus Jakarta Sans
│   │   └── network/
│   │       ├── http_client.dart            # Dio/Http ኢንተርሴፕተሮች እና ቶከን ማረጋገጫ
│   │       └── error_handler.dart          # የኔትወርክ እና የክፍያ ውድቀት ማስተናገጃ
│   │
│   ├── features/                           # ሞዱላር የሆኑ የስራ ክፍሎች
│   │   ├── home/                           # የመነሻ ዳሽቦርድ፣ ኢቨንት ስላይደር እና ምድቦች
│   │   │   ├── presentation/
│   │   │   │   ├── screens/
│   │   │   │   │   ├── home_dashboard_screen.dart
│   │   │   │   │   └── home_with_slider_screen.dart
│   │   │   │   └── widgets/
│   │   │   │       ├── category_grid.dart
│   │   │   │       └── vip_promo_banner.dart
│   │   ├── auth/                           # የስልክ ቁጥር እና የኦቲፒ (OTP) መለያ መግቢያ
│   │   ├── listings/                       # የሽያጭ እና የኪራይ ካታሎግ፣ የዕቃ ዝርዝር ገጽ
│   │   ├── post_listing/                   # የሻጭ ማስታወቂያ መለጠፊያ እና የፎቶ ማያያዣ
│   │   ├── payments/                       # የቴሌብር እና ሲቢኢ ብር ኤፒአይ ክፍያዎች
│   │   │   ├── presentation/
│   │   │   │   ├── screens/
│   │   │   │   │   ├── telebirr_checkout_screen.dart
│   │   │   │   │   ├── cbe_birr_checkout_screen.dart
│   │   │   │   │   ├── payment_retry_fallback_screen.dart
│   │   │   │   │   └── payment_success_invoice_screen.dart
│   │   │   │   └── widgets/
│   │   │   │       └── unlock_confetti_animation.dart
│   │   ├── tenders_rfq/                    # የተገላቢጦሽ ጨረታ (Buyer RFQ & Submit Bid)
│   │   │   ├── presentation/
│   │   │   │   ├── screens/
│   │   │   │   │   ├── tenders_hub_screen.dart
│   │   │   │   │   ├── post_buyer_rfq_screen.dart
│   │   │   │   │   └── unlocked_tender_detail_screen.dart
│   │   │   │   └── widgets/
│   │   │   │       └── submit_bid_modal.dart
│   │   ├── chat/                           # የቀጥታ ውይይት እና የዋጋ ድርድር (Make Offer)
│   │   └── wallet/                         # የዲጂታል የኪስ ቦርሳ፣ ሂሳብ መሙያ እና ማውጫ
│   │
│   └── shared_widgets/                     # በሁሉም ገጽ የሚሰሩ ወጥ አካላት
│       ├── bottom_nav_bar.dart             # ባለ 5 ቁልፍ ወጥ የታችኛው ማሰሻ
│       ├── top_app_bar.dart                # የደሴ ማርት ራስጌ እና የፍለጋ አሞሌ
│       └── custom_toast.dart
│
├── server/                                 # ⚡ Node.js / Express Backend & Microservices
│   ├── src/
│   │   ├── app.js                          # ኤክስፕረስ አፕ እና ሚድልዌሮች
│   │   ├── server.js                       # HTTP & WebSocket ሰርቨር ማስጀመሪያ
│   │   ├── controllers/
│   │   │   ├── paymentWebhookController.js # የቴሌብር እና ሲቢኢ ብር ሁለንተናዊ ዌብሁክ
│   │   │   ├── listingController.js        # የማስታወቂያዎች CRUD እና ፍለጋ
│   │   │   ├── tenderController.js         # የጨረታ እና የ 50 ብር ሰነድ መክፈቻ
│   │   │   └── walletController.js         # የዋሌት ቀሪ ሂሳብ እና ክፍያዎች
│   │   ├── services/
│   │   │   ├── telebirrService.js          # የቴሌብር H5 / Web Checkout ጥሪ ማመንጫ
│   │   │   ├── cbeBirrService.js           # የሲቢኢ ብር WebPay ኤፒአይ
│   │   │   ├── telegramBotService.js       # ወደ @DessieMarket ማስታወቂያ ማሰራጫ ቦት
│   │   │   └── idempotencyService.js       # ድርብ ክፍያ መከላከያ እና አውቶ-ተመላሽ
│   │   └── db/
│   │       ├── migrations/                 # የ PostgreSQL ዳታቤዝ ሰንጠረዦች
│   │       └── prisma/
│   │           └── schema.prisma           # የዳታቤዝ ሞዴሎች (Users, Listings, Tenders)
│   ├── tests/                              # cURL እና ጄስት (Jest) የዌብሁክ ቴስቶች
│   ├── Dockerfile                          # የፕሮዳክሽን Docker ምስል ማዘጋጃ
│   └── package.json
│
├── scripts/                                # 🛠️ አጋዥ እና አውቶሜሽን ስክሪፕቶች
│   ├── generate_keystore.sh                # የፕሮዳክሽን Keystore ማመንጫ ስክሪፕት
│   ├── simulate_webhooks.sh                # የቴሌብር እና ሲቢኢ ክፍያ መሞከሪያ
│   └── db_backup.sh                        # የዳታቤዝ እለታዊ መጠባበቂያ
│
├── assets/                                 # 🎨 ምስሎች፣ አዶዎችና ሎጎዎች
│   ├── logo/
│   │   ├── dessie_mart_logo.svg            # የታሪካዊው ሙጋድ አዳራሽ ይፋዊ ሎጎ
│   │   └── dessie_mart_logo.png
│   ├── icons/
│   │   ├── app_icon_squircle.png           # የመተግበሪያ አዶ (Android / iOS)
│   │   └── payment_gateways/               # የቴሌብር እና ሲቢኢ ብር አርማዎች
│   └── marketing/
│       └── promo_poster.png                # የደሴ ማርት ይፋዊ የማስተዋወቂያ ፖስተር
│
├── docs/                                   # 📑 የፕሮጀክቱ ሙሉ ሰነዶች (Documentation)
│   ├── GO_LIVE_RUNBOOK.md                  # ይፋዊ የፕሮዳክሽን ማሰማሪያ ፍኖተ-ካርታ
│   ├── SANDBOX_TESTING_GUIDE.md            # የቴሌብር እና ሲቢኢ ብር የሳንድቦክስ ፍተሻ መመሪያ
│   ├── PAYMENT_TENDER_LIFECYCLE.md         # የክፍያ እና የጨረታ ፍሰት ማጠቃለያ
│   └── APK_AAB_BUILD_GUIDE.md              # የአንድሮይድ መተግበሪያ ግንባታ መመሪያ
│
├── .env.example                            # የፕሮዳክሽን እና የሳንድቦክስ ሚስጥራዊ ቁልፎች ናሙና
├── .gitignore                              # Git ውስጥ እንዳይገቡ የተከለከሉ ፋይሎች (Keys, .env)
├── docker-compose.yml                      # ለሎካል ልማት (Backend + PostgreSQL + Redis)
├── pubspec.yaml                            # የ Flutter ፓኬጆችና ዲፔንደንሲዎች ዝርዝር
└── README.md                               # የፕሮጀክቱ ዋና መግለጫ እና የማስጀመሪያ መመሪያ
```

---

## 🔑 3. ቁልፍ የፎልደር ክፍሎች ማብራሪያ (Key Directory Highlights)

1. **`.github/workflows/` (CI/CD):** 
   ገንቢዎች ኮዱን `main` ብራንች ላይ ሲገፉ የ **Android APK እና AAB** ጥቅልን በራስ-ሰር ቆርጦ የሚያዘጋጅ እና ሰርቨሩን የሚያሰማራ አውቶሜሽን።
2. **`lib/features/payments/` & `lib/features/tenders_rfq/` (Mobile Features):**
   የ 50 ብር የጨረታ ሰነድ መክፈቻ፣ የ 100 ብር የህትመት ክፍያ፣ የቴሌብር/ሲቢኢ ፈጣን ጌትዌዮች እና ውድቀት ሲያጋጥም የሚከፈተውን የድጋሚ መክፈያ (Fallback) ስክሪን የያዘ ነው።
3. **`server/services/telegramBotService.js`:**
   ክፍያው እንደተጠናቀቀ ማስታወቂያውን ወዲያውኑ ወደ **`@DessieMarket`** ቴሌግራም ቻናል በፎቶና በዋጋ የሚለጥፈው አውቶሜትድ ቦት።
4. **`android/app/proguard-rules.pro`:**
   የአማርኛ ፊደላት፣ የባንክ ኤፒአይ ሞዴሎችና የቴሌብር ክፍያ ክፍሎች ኮዱ በሚጨመቅበት ወቅት (Code Minification) እንዳይሰበሩ የሚያረጋግጥ።

---
*ይህ ሰነድ ለደሴ ማርት (ሙጋድ ገበያ) ይፋዊ የ GitHub ሪፖዚቶሪ መዋቅር ሆኖ የተዘጋጀ ሙሉ ማውጫ ነው።*
