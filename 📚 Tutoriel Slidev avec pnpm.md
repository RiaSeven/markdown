# 📚 Tutoriel Slidev avec pnpm

Ce tutoriel t'accompagne pas à pas pour créer un diaporama moderne et interactif en utilisant Slidev, pnpm, Git, GitHub, StackBlitz, et VS Code.

## 🚩 1. Installation des pré-requis

### Outils nécessaires :

* Windows 10 (64 bits)
* [Node.js LTS](https://nodejs.org)
* [Git](https://git-scm.com)
* [VS Code](https://code.visualstudio.com)
* Un compte [GitHub](https://github.com)

### Installer pnpm

Ouvre PowerShell et tape :

```shell
npm install -g pnpm
```

Vérifie l’installation :

```shell
pnpm -v
```

---

## 🚩 2. Création du projet Slidev

Crée ton diaporama Slidev avec pnpm :

```shell
pnpm create slidev@latest
```

Réponds aux questions interactives (nom du projet, thème par défaut).

Entre dans ton dossier :

```shell
cd mon-diaporama
pnpm dev
```

Accède à `http://localhost:3030`.

---

## 🚩 3. Initialisation Git

Ouvre ton terminal dans ton dossier :

```shell
git init
git add .
git commit -m "Initialisation Slidev avec pnpm"
```

Configure ton identité Git (si nécessaire) :

```shell
git config --global user.name "TonNom"
git config --global user.email "ton-email@example.com"
```

---

## 🚩 4. Hébergement sur GitHub

* Va sur [GitHub](https://github.com), crée un nouveau dépôt : `mon-diaporama-slidev`
* Sans README, gitignore, ni licence pour l'instant.

Dans ton terminal :

```shell
git remote add origin https://github.com/TON_USERNAME/mon-diaporama-slidev.git
git branch -M main
git push -u origin main
```

---

## 🚩 5. Édition des diapositives en Markdown

### Localement (VS Code)

* Ouvre le dossier dans VS Code.
* Édite `slides.md`.
* Sépare chaque diapositive par :

```markdown
---
```

### Exemple Markdown :

```markdown
# Première Slide
Bienvenue sur Slidev !

---

## Slide suivante
- Item 1
- Item 2
```

Visualise avec :

```shell
pnpm dev
```

### En ligne (StackBlitz)

* Va sur [stackblitz.com](https://stackblitz.com).
* Importe ton dépôt GitHub.
* Édite directement en ligne.

---

## 🚩 6. Publication GitHub Pages

Génère la version statique localement :

```shell
pnpm build
```

Ajoute le dossier `dist` à Git :

```shell
git add dist -f
git commit -m "Build des diapositives"
git push origin main
```

Sur GitHub :

* Va dans ton dépôt → `Settings` → `Pages`
* Choisis branche `main` et dossier `/dist`.
* Tes diapositives seront disponibles sur :

```
https://TON_USERNAME.github.io/mon-diaporama-slidev/
```

---

## 🚩 7. Personnaliser thèmes et styles

### Changer de thème

Dans `slides.md` en haut :

```yaml
---
theme: seriph
---
```

Thèmes populaires :

* `default`
* `seriph`
* `apple-basic`
* `dracula`

### Styles personnalisés

Modifie `styles/global.css` :

```css
.slidev-layout {
  color: #333;
}

body {
  background-color: #f0f4f8;
}
```

---

## 🚩 8. Workflow recommandé

```
Édition locale (VS Code)
↓
Prévisualisation (pnpm dev)
↓
Build (pnpm build)
↓
Commit régulier Git
↓
Push GitHub
↓
Publication GitHub Pages
```

---

## 🎯 Conclusion

Tu es maintenant capable de créer, personnaliser et publier un diaporama moderne et interactif grâce à Slidev et pnpm !

---

📌 **Ressources utiles** :

* [Slidev](https://sli.dev)
* [pnpm](https://pnpm.io)
* [StackBlitz](https://stackblitz.com)
* [GitHub Pages](https://pages.github.com)

🎉 Bonne création de diaporama !

