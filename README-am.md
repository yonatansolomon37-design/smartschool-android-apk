# SmartSchool - Android App Project (Capacitor)

## ለምን ዝግጁ የAPK ፋይል የለም?
ይህ Claude የሚሰራበት አካባቢ ወደ Google/Android SDK እና Gradle አገልጋዮች የኢንተርኔት መዳረሻ ስለሌለው፣ የመጨረሻውን .apk ፋይል በቀጥታ መገንባት (compile ማድረግ) አልቻለም። ግን ሙሉ የAndroid Studio ፕሮጀክት (Capacitor) ተዘጋጅቷል — ግንባታው (build) ብቻ ቀርቷል፣ እሱም ከሚከተሉት 2 መንገዶች በአንዱ በቀላሉ ይሆናል።

## መንገድ 1 - Android Studio በኮምፒውተርዎ (ይመከራል፣ ቀላል)
1. Android Studio ያውርዱ፣ ይጫኑ፡ https://developer.android.com/studio
2. ይህን ፎልደር ሙሉውን ይክፈቱ (Open an existing project) → `android` የሚለውን ፎልደር ይምረጡ
3. Android Studio ራሱ SDK/Gradle በራስ-ሰር ያወርዳል (የመጀመሪያ ጊዜ ትንሽ ጊዜ ይወስዳል)
4. ላይ ካለው ምናሌ: Build → Build Bundle(s)/APK(s) → Build APK(s)
5. የተጠናቀቀው APK እዚህ ይገኛል፡ `android/app/build/outputs/apk/debug/app-debug.apk`
6. ያንን ፋይል ወደ ስልክዎ ገልብጠው ይጫኑት (ከ"Unknown sources" ማብራት ያስፈልጋል)

## መንገድ 2 - GitHub Actions (ኮምፒውተር ላይ ምንም ሳይጭኑ፣ ነጻ)
1. በ https://github.com ነጻ አካውንት ይክፈቱ (ካልነበረዎት)
2. አዲስ repository ይፍጠሩ (ለምሳሌ smartschool-app)
3. ይህን ሙሉ ፎልደር (ከ .github ፎልደር ጋር) ወደዚያ repository ይስቀሉ (upload files በድረ-ገጽ በኩል በቀጥታ መጠቀም ይቻላል)
4. ወደ repository ውስጥ "Actions" tab ይሂዱ → "Build Android APK" workflow በራስ-ሰር ይሰራል (2-3 ደቂቃ ይወስዳል)
5. ሲጨርስ በዚያው ገጽ ስር "Artifacts" ውስጥ smartschool-debug-apk የሚለውን ያውርዱ

## ማስታወሻ
- App ID: com.solomonarega.smartschool
- ይህ የሚፈጠረው "debug" APK ለሙከራ/ለውስጥ ስርጭት ተስማሚ ነው። ለPlay Store ማውጣት ካሰቡ "release" build እና ፊርማ (signing key) ያስፈልጋል - ካስፈለገ ያንን ደረጃ ደግሜ ልርዳዎት እችላለሁ።
