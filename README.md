<div align="center">
  <a href="https://tools.techsentinel.fr"><img src="docs/assets/techsentinel-toolbox-hero.svg" width="100%" alt="Bannière TechSentinel Toolbox — interface conceptuelle des outils image, PDF, texte et données"></a>
  <br><br><img src="src/assets/logo.png" width="120" alt="Logo TechSentinel Toolbox" />
  <br /><br />
  <h1>TechSentinel Toolbox</h1>
  <p><strong>Outils gratuits pour convertir, éditer, calculer et gagner du temps — dans votre navigateur.</strong></p>
  <p><a href="https://tools.techsentinel.fr"><strong>Essayer les outils</strong></a> · <a href="#-fonctionnalités">Fonctionnalités</a> · <a href="#-installation--déploiement">Auto-hébergement</a> · <a href="#️-développement">Contribuer</a></p>
  <p><a href="LICENSE"><img src="https://img.shields.io/github/license/neosoda/Tools?color=22c9bc" alt="Licence"></a> <img src="https://img.shields.io/badge/Docker-ready-2496ED?logo=docker&logoColor=white" alt="Docker"> <img src="https://img.shields.io/badge/React-%2B%20TypeScript-4e9bdd?logo=react&logoColor=white" alt="React TypeScript"></p>
  <br />
</div>

> **Visuel :** la bannière présente les grandes familles d’outils, mais ne représente pas une capture d’écran de l’application.

| 🖼️ **Médias** | 📄 **Documents** | 🛠️ **Utilitaires** |
| :--- | :--- | :--- |
| Images, vidéo, audio et conversion. | Fusion, découpe et édition PDF. | Texte, listes, dates, maths, JSON, CSV et XML. |

## 📋 À propos

**TechSentinel Toolbox** est une application web auto-hébergée offrant une variété d'outils en ligne pour simplifier vos tâches quotidiennes. Que vous travailliez avec des images, des vidéos, des PDFs, du texte ou des données, TechSentinel Toolbox vous accompagne.

**Sécurité et confidentialité** : Tous les fichiers sont traités entièrement côté client. Rien ne quitte jamais votre appareil.

**Déploiement** : l’application est compilée avec Vite puis servie par Nginx dans une image Docker multi-étapes. Aucune taille fixe de l’image n’est garantie ici.


## ✨ Fonctionnalités

### 🖼️ **Outils Image/Vidéo/Audio**
- Redimensionneur d'images
- Convertisseur d'images
- Éditeur d'images
- Découpe vidéo
- Inversion vidéo
- Et bien plus...

### 📄 **Outils PDF**
- Diviseur PDF
- Fusionneur PDF
- Éditeur PDF
- Et bien plus...

### 📝 **Outils Texte/Liste**
- Convertisseurs de casse
- Mélangeur de listes
- Formateurs de texte
- Et bien plus...

### 🕐 **Outils Date et Heure**
- Calculateurs de dates
- Convertisseurs de fuseaux horaires
- Et bien plus...

### 🔢 **Outils Mathématiques**
- Générateur de nombres premiers
- Calculateur de tension, courant, résistance
- Et bien plus...

### 💾 **Outils de Données**
- Outils JSON
- Outils CSV
- Outils XML
- Et bien plus...

## 🚀 Installation & Déploiement

### Docker

```bash
docker build -t techsentinel-toolbox .
docker run -d --name techsentinel-toolbox --restart unless-stopped -p 8080:3000 techsentinel-toolbox
```

### Docker Compose

```yaml
services:
  techsentinel-toolbox:
    build: .
    container_name: techsentinel-toolbox
    restart: unless-stopped
    ports:
      - "8080:3000"
```

### Déploiement Coolify

TechSentinel Toolbox est entièrement compatible avec [Coolify](https://coolify.io).

#### Démarrage rapide

1. **Créer une nouvelle application dans Coolify**
   - Type : Application
   - Source : Public Repository

2. **Configurer le dépôt**
   - URL : `https://github.com/neosoda/Tools`
   - Branche : `main`
   - Build Pack : `Dockerfile`

3. **Configurer les paramètres de déploiement**
   - Port : `3000` (interne)
   - Healthcheck Path : `/health`
   - Healthcheck Interval : `30s`

4. **Déployer**
   - Cliquez sur "Deploy"
   - Accédez à votre application via l'URL fournie

#### Variables d'environnement

| Variable | Description | Par défaut | Requis |
|----------|-------------|------------|--------|
| `PORT` | Port externe | `8080` | Non |
| `NODE_ENV` | Environnement Node | `production` | Non |
| `LOCIZE_API_KEY` | Clé API pour traductions | - | Non |

## 🛠️ Développement

### Configuration du projet

```bash
git clone https://github.com/neosoda/Tools.git
cd Tools
npm install
npm run dev
```

### Créer un nouvel outil

```bash
npm run script:create:tool mon-outil-nom dossier1
```

Pour les outils dans des répertoires imbriqués :

```bash
npm run script:create:tool compress image/png
```

### Exécuter les tests

```bash
npm run test        # Tests unitaires
npm run test:e2e    # Tests end-to-end
```

### Traductions (i18n)

Les fichiers de traduction sont disponibles dans [public/locales](public/locales).

## 🤝 Contribuer

Les contributions sont les bienvenues ! Vous pouvez aider en :

- Signalant des bugs
- Suggérant de nouvelles fonctionnalités
- Améliorant la documentation
- Soumettant des pull requests

## Origine et attribution

**TechSentinel Toolbox** reprend une base du projet open source [OmniTools](https://github.com/iib0011/omni-tools), créé par **Ibrahima Gaye Coulibaly**, puis adaptée pour l'écosystème TechSentinel. Le projet d'origine est publié sous **licence MIT** ; son copyright et les notices correspondantes doivent être conservés. Voir [LICENSE](LICENSE).

Les développements et adaptations propres à TechSentinel ne remplacent pas les droits des contributeurs d'origine.

## 📧 Contact

Pour toute question ou suggestion :
**[contact@techsentinel.fr](mailto:contact@techsentinel.fr)**

## Questions fréquentes

**Peut-on utiliser TechSentinel Toolbox sans installer de logiciel ?** Oui : ouvrez [tools.techsentinel.fr](https://tools.techsentinel.fr) depuis un navigateur moderne.

**Peut-on auto-héberger cette boîte à outils ?** Oui, le `Dockerfile` et l'exemple Docker Compose sont fournis dans ce dépôt.

**À qui s'adresse-t-elle ?** Aux particuliers, développeurs, administrateurs et équipes qui cherchent des convertisseurs et utilitaires web simples, sans multiplier les sites.

## 📜 Licence

Ce projet est sous licence MIT. Consultez le fichier [LICENSE](LICENSE) pour plus de détails.

---

<div align="center">
  <p>Développé avec ❤️ par <strong>TechSentinel</strong></p>
  <p><a href="https://techsentinel.fr">techsentinel.fr</a></p>
</div>
