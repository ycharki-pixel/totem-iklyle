# Totem IKLYLE - Application Android

Application d'affichage publicitaire pour les totems des Centres Culturels IKLYLE
Fondation Mohammed VI pour la Promotion des Œuvres Sociales de l'Éducation-Formation

---

## 🚀 MÉTHODE RAPIDE : Compiler via GitHub (Recommandé)

**Obtenez votre APK en 5 minutes sans installer Android Studio !**

### Étapes :

1. **Créer un compte GitHub** (gratuit) sur https://github.com si vous n'en avez pas

2. **Créer un nouveau repository** :
   - Cliquez sur "+" → "New repository"
   - Nom : `totem-iklyle`
   - Visibilité : Public ou Private
   - Cliquez "Create repository"

3. **Uploader les fichiers** :
   - Sur la page du repository, cliquez "uploading an existing file"
   - Glissez-déposez TOUS les fichiers du dossier `totem-android`
   - Cliquez "Commit changes"

4. **Lancer la compilation** :
   - Allez dans l'onglet "Actions"
   - Cliquez sur "Build Android APK"
   - Cliquez "Run workflow" → "Run workflow"

5. **Télécharger l'APK** :
   - Attendez ~3-5 minutes que le build soit vert ✅
   - Cliquez sur le build terminé
   - Dans "Artifacts", téléchargez `totem-iklyle-debug`

**C'est tout ! Votre APK est prêt à être installé.**

---

## 📱 Fonctionnalités

- ✅ Affichage plein écran (mode kiosk)
- ✅ Diaporama automatique avec transitions fluides
- ✅ Sélection du centre culturel (Rabat, Casablanca, Fès, Tanger, Tétouan, Oujda)
- ✅ Durée d'affichage paramétrable
- ✅ Import d'images depuis la galerie
- ✅ Sauvegarde automatique de la configuration
- ✅ Écran toujours allumé
- ✅ Mode paysage optimisé pour les totems

## 🛠️ Prérequis

- Android Studio Hedgehog (2023.1.1) ou plus récent
- JDK 17
- Android SDK 34
- Un appareil Android (API 24+, Android 7.0 ou supérieur)

## 📦 Installation

### Option 1 : Compilation avec Android Studio

1. **Ouvrir le projet**
   - Lancez Android Studio
   - Sélectionnez "Open" et naviguez vers le dossier `totem-android`
   - Attendez que Gradle synchronise le projet

2. **Compiler l'APK**
   - Menu : Build → Build Bundle(s) / APK(s) → Build APK(s)
   - L'APK sera généré dans : `app/build/outputs/apk/debug/app-debug.apk`

3. **Installer sur l'appareil**
   - Connectez votre appareil Android via USB
   - Activez le "Débogage USB" dans les options développeur
   - Cliquez sur "Run" (▶️) dans Android Studio

### Option 2 : Compilation en ligne de commande

```bash
# Se placer dans le dossier du projet
cd totem-android

# Compiler l'APK de debug
./gradlew assembleDebug

# L'APK sera dans : app/build/outputs/apk/debug/app-debug.apk
```

### Option 3 : Générer un APK signé (Production)

1. Dans Android Studio : Build → Generate Signed Bundle / APK
2. Sélectionnez "APK"
3. Créez ou utilisez un keystore existant
4. Sélectionnez "release" comme build variant
5. L'APK signé sera prêt pour distribution

## 🚀 Utilisation

1. **Lancer l'application** sur le totem/tablette
2. **Toucher l'écran** pour faire apparaître le bouton de configuration (⚙️)
3. **Configurer** :
   - Sélectionner le centre culturel
   - Définir la durée d'affichage
   - Ajouter les images publicitaires
4. **Lancer le diaporama** avec le bouton vert

## 📁 Structure du projet

```
totem-android/
├── app/
│   ├── src/main/
│   │   ├── assets/
│   │   │   └── index.html          # Interface web
│   │   ├── java/.../
│   │   │   └── MainActivity.kt     # Activité principale
│   │   ├── res/
│   │   │   ├── layout/             # Layouts XML
│   │   │   ├── values/             # Ressources (strings, colors, themes)
│   │   │   └── drawable/           # Icônes
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── build.gradle
└── settings.gradle
```

## ⚙️ Configuration pour mode Kiosk

Pour verrouiller l'application en mode totem :

1. **Épinglage d'écran** (Android natif) :
   - Paramètres → Sécurité → Épinglage d'écran → Activer
   - Ouvrir l'application, appuyer sur Aperçu, épingler

2. **Mode propriétaire d'appareil** (recommandé pour déploiement) :
   - Utiliser un MDM (Mobile Device Management)
   - Ou configurer via ADB en mode device owner

## 🔧 Personnalisation

### Modifier les centres culturels

Éditer le fichier `app/src/main/assets/index.html`, section `<select id="selectCenter">` :

```html
<option value="Centre Culturel IKLYLE - Nouveau">Nouveau Centre</option>
```

### Modifier les couleurs

Éditer `app/src/main/res/values/colors.xml` :

```xml
<color name="primary_green">#1B5E3B</color>
<color name="accent_gold">#C9A227</color>
```

## 📞 Support

Pour toute question technique :
- Chef de Service des Centres Culturels IKLYLE
- Fondation Mohammed VI pour la Promotion des Œuvres Sociales de l'Éducation-Formation

---

**Version** : 1.0  
**Compatibilité** : Android 7.0+ (API 24+)  
**Orientation** : Paysage (landscape)
