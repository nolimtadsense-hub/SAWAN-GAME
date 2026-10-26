# FIGHTER FTR APP — Android Starter Project

यह Android Studio के लिए शुरुआती Kotlin + Jetpack Compose प्रोजेक्ट है।

## अभी क्या है?
- FIGHTER FTR APP का शुरुआती Android UI
- Login / Register स्क्रीन का UI
- Chat स्क्रीन का UI और संदेश लिखने का स्थानीय डेमो
- Status, Photo, Voice के लिए शुरुआती navigation/placeholder
- Firebase जोड़ने के निर्देश

## जरूरी बात
यह अभी तैयार APK नहीं है। Login, अलग-अलग मोबाइलों के बीच real-time chat, photo upload, voice recording और status को असली तरह चलाने के लिए Firebase project/configuration और implementation पूरा करना होगा। इस zip में कोई निजी API key या Firebase config शामिल नहीं है।

## Android Studio में खोलें
1. कंप्यूटर पर Android Studio इंस्टॉल करें।
2. इस फ़ोल्डर को Android Studio में Open करें।
3. Gradle sync पूरा होने दें।
4. Emulator या Android फोन पर Run करें।

## Firebase जोड़ना (real login/chat के लिए)
1. Firebase Console में नया project बनाएं और Android app package `com.fighterftr.app` जोड़ें।
2. `google-services.json` डाउनलोड करके `app/` फ़ोल्डर में रखें।
3. Firebase Authentication में Email/Password enable करें।
4. Firestore Database enable करें; production में secure rules लगाएं।
5. Photo/status uploads के लिए Firebase Storage enable करें।
6. `app/build.gradle.kts` में Firebase dependencies और Google Services plugin जोड़ें (नीचे टिप्पणी वाला template देखें)। फिर Login/Chat UI को Firebase Auth/Firestore/Storage से जोड़ें।

## फोन पर ही काम करना है?
सिर्फ इस zip को डाउनलोड करने से APK अपने-आप नहीं बनता। APK बनाने के लिए Android build environment (जैसे Android Studio वाला कंप्यूटर, या compatible cloud build) चाहिए।

## Friend Request सिस्टम (डेमो)
- Friends स्क्रीन में username डालकर request भेजने का UI।
- Requests स्क्रीन में sample incoming requests को Accept/Reject करने का UI।
- Accept करने पर user My Friends list में जुड़ता है।
- अभी यह local demo है; अलग-अलग devices पर असली requests के लिए Firebase Authentication + Firestore rules/collections जोड़ना जरूरी है।
