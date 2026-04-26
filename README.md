# lab6_sec
📱 Rapport d’analyse statique — Pizza Recipes APK
📌 Informations générales
ChampValeur📦 APK analysépizza.apk🔐 SHA-2567def8c514f65bcb1d92403945d498618e0567dbd51b40796da4acf0f1aeb7cd6🛠️ OutilMobSF v4.5.0🧪 Version APK1.0

🧠 Résumé exécutif
L’application présente un niveau de sécurité :

🚨 CRITICAL RISK — Score : 27/100 (F)

⚠️ Problèmes majeurs :


Mauvaise configuration de sécurité Android


Signature non sécurisée


Mode debug activé


Composants obsolètes



⚠️ Vulnérabilités critiques

🔴 1. Signature avec certificat de débogage
Sévérité : ÉLEVÉE
CN=Android Debug, O=Android, C=US
💥 Impact


Signature non fiable


Risque de falsification


Non conforme production


✅ Remédiation


Utiliser un certificat de production sécurisé



🔴 2. Algorithme de signature SHA1
Sévérité : ÉLEVÉE
💥 Impact


Vulnérable aux attaques par collision


✅ Remédiation


Migrer vers SHA-256



🔴 3. Version Android obsolète
Sévérité : ÉLEVÉE
minSdkVersion = 17
💥 Impact


Support de versions Android non sécurisées


Surface d’attaque élevée


✅ Remédiation


Passer à API 29+



🔴 4. Mode débogage activé
Sévérité : ÉLEVÉE
android:debuggable="true"
💥 Impact


Analyse dynamique facilitée


Accès ADB simplifié


✅ Remédiation


Désactiver en production



⚠️ Autres observations

🟠 Janus Vulnerability


Risque sur anciennes versions Android


Compatibilité signatures anciennes



🟠 Backup activé
android:allowBackup="true"
💥 Impact


Extraction possible via ADB



📊 Résumé sécurité
ÉlémentÉtatSignature❌ DebugAlgorithme❌ SHA1Debug mode❌ ActivéVersion Android❌ ObsolèteScore global⚠️ 27/100

🎯 Recommandations
🔥 Critiques


Re-signer l’application en production


Désactiver debug mode


⚙️ Système


Mettre à jour minSdkVersion (≥ 29)


Désactiver allowBackup


🔐 Cryptographie


Remplacer SHA1 par SHA-256



📸 Annexes
🐳 Déploiement MobSF
docker pull opensecurity/mobile-security-framework-mobsf
docker run -it -p 8000:8000 mobsf

📊 Résultats MobSF


Score global : 27/100


Niveau : CRITICAL RISK


Analyse complète réussie



🧠 Conclusion
L’application présente plusieurs mauvaises pratiques de sécurité :


❌ Mauvaise configuration Android


❌ Mode debug activé


❌ Algorithmes obsolètes


👉 Elle n’est pas adaptée à un environnement de production sécurisé.

Si tu veux, je peux maintenant te faire :


🔥 un template unique pour tous tes rapports APK (Level 1, 2, MobSF)


📊 un GitHub portfolio pentest complet stylé bug bounty


🧠 ou une version PDF professionnelle prête pour stage

