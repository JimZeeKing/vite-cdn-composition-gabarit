# Explication Courte du Gabarit Vue.js avec Composition API

Voici une brève explication du gabarit pour une application Vue.js utilisant le **Composition API** avec les modules ESM via CDN.

---

## Code du Gabarit

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Démarrage Vue.js avec Composition API</title>
</head>
<body>
  <div id="app">
    {{ message }}
  </div>

  <script type="module">
    import { createApp, ref } from 'https://unpkg.com/vue@3/dist/vue.esm-browser.js';

    createApp({
      setup() {
        const message = ref('Bonjour Vue.js avec Composition API !');
        return { message };
      }
    }).mount('#app');
  </script>
</body>
</html>
```

---

## Explication Rapide

- **Importation de Vue.js :**
  - On utilise le CDN `unpkg.com` pour importer `createApp` et `ref` depuis Vue.js.
  - Le script est de type `module` pour permettre l'utilisation de `import`.

- **Création de l'Application :**
  - `createApp({ ... }).mount('#app')` crée et monte l'application sur l'élément avec l'id `app`.

- **Utilisation du Composition API :**
  - La fonction `setup()` est le point d'entrée du Composition API.
  - `const message = ref('...')` crée une variable réactive `message`.
  - `return { message }` rend `message` accessible dans le template.

- **Affichage dans le Template :**
  - `{{ message }}` affiche la valeur de `message` dans l'élément `div`.

---

Ce gabarit simple vous permet de démarrer rapidement avec Vue.js en utilisant le Composition API et le module ESM via CDN.
