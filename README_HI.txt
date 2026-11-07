NOOR-E-NAMAZ — Android project with your Adhan audio

इस पैकेज में:
- Android ऐप का source code और WebView में खुलने वाला Quran/HTML पेज
- आपकी अपलोड की हुई azan2.mp3, ऐप में app/src/main/res/raw/adhan.mp3 नाम से
- Kolkata के लिए AlAdhan API से आज और अगले दिन के पाँच नमाज़ समय
- पाँचों नमाज़ों के लिए Android alarm scheduling code
- फोन restart / समय या timezone बदलने पर alarm refresh
- GitHub Actions workflow: cloud में debug APK बनाने के लिए

महत्वपूर्ण:
- इस पैकेज में APK पहले से नहीं है। इस वातावरण में Android SDK उपलब्ध नहीं है, इसलिए APK compile/test नहीं हुआ।
- नमाज़ के समय स्थानीय मस्जिद के timetable से मिलाएँ। अभी Kolkata और Karachi calculation method (method=1) default हैं।
- समय refresh करने के लिए internet चाहिए। Android में notifications और Alarms & reminders permissions दें।
- फोन की battery restrictions background alarm को प्रभावित कर सकती हैं।

फोन से APK बनाने का तरीका:
1. ZIP को GitHub पर एक नए repository में upload करें और project की अंदर की सभी files रखें।
2. Repository में Actions tab खोलें।
3. “Build Noor-e-Namaz APK” workflow चुनें और Run workflow दबाएँ (push पर भी build शुरू होगा)।
4. पूरा होने पर workflow run खोलें, नीचे Artifacts में Noor-e-Namaz-debug-apk डाउनलोड करें।
5. ZIP artifact खोलकर app-debug.apk फोन में डाउनलोड करें और install करें। Android पूछे तो इस स्रोत से install की अनुमति दें।

यह cloud build workflow है; APK बनने के बाद भी वास्तविक फोन पर permissions, नमाज़ समय और अज़ान playback की जाँच ज़रूरी है।
