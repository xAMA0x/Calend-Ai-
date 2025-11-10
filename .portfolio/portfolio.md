---
title: "Calend-Ai"
description: "Application mobile de calendrier intelligent construite avec React Native / Expo et JavaScript."
date: "2024-04-24"
tags: ["javascript","react-native","mobile","expo","calendrier"]
lang: "fr"

# Configuration techStack
techStack:
  - name: "JavaScript"
    category: "language"
    icon: "📜"
  - name: "React Native"
    category: "framework"
    icon: "⚛️"
  - name: "Expo"
    category: "tool"
    icon: "🚀"
  - name: "React Navigation"
    category: "framework"
    icon: "🧭"
  - name: "Formik / Yup"
    category: "tool"
    icon: "📝"
  - name: "SQLite"
    category: "database"
    icon: "💾"
  - name: "IA / Modèle intelligent"
    category: "tool"
    icon: "🧠"

# Architecture du projet
architecture:
  overview: "L'architecture est une application mobile monolithique (front-end seul) typique de React Native/Expo. Le cœur de l'application est en JavaScript et repose sur la navigation par piles (React Navigation). La logique métier (gestion des événements, des tâches et de l'intelligence) est étroitement liée à l'interface utilisateur. La persistence des données (événements, utilisateurs) s'effectue via un stockage local asynchrone pour garantir une utilisation hors ligne fluide."
  components:
    - "Cœur React Native (JavaScript) : Gère le rendu de l'UI, le cycle de vie des composants et la logique de manipulation du DOM virtuel."
    - "React Navigation (Routing) : Gère la navigation entre les écrans (ex: Écran Calendrier, Écran Tâches, Écran Configuration) via un système de piles."
    - "Persistence Locale (Stockage asynchrone / SQLite) : Stocke les données des événements, des tâches et des utilisateurs directement sur l'appareil pour garantir l'accès hors ligne."
    - "Logique IA / Moteur de Suggestion : Module central pour l'aspect intelligent du projet. Gère l'analyse des tâches, la détection des conflits d'horaire, et propose des suggestions d'ordonnancement."
    - "Formulaires (Formik / Yup) : Gère la création et la validation des formulaires complexes (ajout d'événements, modifications de tâches)."

# Diagrammes d'architecture (optionnel)
diagrams:
  - path: "https://raw.githubusercontent.com/xAMA0x/Calend-Ai-/main/.portfolio/diagrams/diagram.svg"
    title: "Architecture Mobile (React Native)"
    description: "Flux de données et séparation des modules dans l'application mobile."

# URLs et liens
demo_url: ""
demo_label: ""
github_url: "https://github.com/xAMA0x/Calend-Ai-"
---

## 🎯 Vue d'ensemble

<div class="overview-hero dark:bg-gradient-to-br dark:from-accent/10 dark:to-purple-900/10 bg-gradient-to-br from-indigo-50 to-purple-50 border dark:border-accent/20 border-indigo-200 rounded-2xl p-8 my-8 shadow-lg">
  <p class="text-lg dark:text-white/90 text-slate-700 leading-relaxed mb-6">
    <strong>Calend-Ai</strong> est un assistant de planification <strong>mobile</strong> qui utilise l'intelligence artificielle pour optimiser votre temps. Développé en <strong>React Native/Expo</strong> dans le cadre d'un projet de groupe de l'ESGI, il analyse vos tâches, détecte les conflits d'horaire et vous propose des <strong>suggestions intelligentes</strong> pour la gestion proactive de votre emploi du temps.
  </p>
  
  <div class="stats-row grid grid-cols-2 md:grid-cols-4 gap-4 mt-6">
    <div class="stat-item text-center">
      <div class="stat-value text-3xl font-bold dark:text-accent text-indigo-600">5</div>
      <div class="stat-label text-sm dark:text-white/60 text-slate-600">Membres de l'équipe (2ème Année)</div>
    </div>
    <div class="stat-item text-center">
      <div class="stat-value text-3xl font-bold dark:text-accent text-indigo-600">100%</div>
      <div class="stat-label text-sm dark:text-white/60 text-slate-600">Technologie Mobile (React Native)</div>
    </div>
    <div class="stat-item text-center">
      <div class="stat-value text-3xl font-bold dark:text-accent text-indigo-600">1</div>
      <div class="stat-label text-sm dark:text-white/60 text-slate-600">Moteur IA / Logique de Suggestion</div>
    </div>
    <div class="stat-item text-center">
      <div class="stat-value text-3xl font-bold dark:text-accent text-indigo-600">1</div>
      <div class="stat-label text-sm dark:text-white/60 text-slate-600">Base de données locale (SQLite)</div>
    </div>
  </div>
</div>

### Objectifs du projet

<div class="objectives-grid grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 my-8">
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      🎓
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Réussite du Projet Annuel
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Délivrer une application complète et fonctionnelle pour l'évaluation de fin de deuxième année à l'ESGI.
    </p>
  </div>
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      ⚛️
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Maîtrise du Mobile (React Native)
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Apprendre et appliquer le framework React Native/Expo pour créer une application native iOS/Android à partir d'une seule base de code.
    </p>
  </div>
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      🧠
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Logique de Suggestion IA
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Développer une logique algorithmique pour détecter les chevauchements et proposer des ajustements d'horaires aux utilisateurs.
    </p>
  </div>
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      🤝
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Travail d'Équipe (5 Membres)
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Gérer la collaboration, le versionnement Git et la répartition des tâches sur un projet front-end conséquent.
    </p>
  </div>
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      💾
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Gérer la Persistence Locale
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Mettre en place une base de données locale (SQLite/AsyncStorage) pour garantir l'accès et la modification des données hors ligne.
    </p>
  </div>
</div>

## ⚛️ Architecture Mobile (React Native)

<div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 my-8">
  <p class="text-sm dark:text-white/70 text-slate-600 leading-relaxed mb-4">
    L'application suit le pattern d'une architecture mobile monolithique basée sur la convention <strong>React Native</strong>. La logique et la vue sont séparées au niveau des composants, le tout étant géré par l'environnement de développement <strong>Expo</strong>.
  </p>
  <ul class="list-disc list-outside space-y-2 pl-5 text-sm dark:text-white/70 text-slate-600">
    <li><strong>Expo Workflow :</strong> Utilisation d'Expo pour la compilation, le test en temps réel et le *bundling* final vers iOS et Android.</li>
    <li><strong>React Navigation :</strong> Le routing est géré par des stacks de navigation pour une expérience utilisateur fluide entre les écrans principaux (Calendrier, Paramètres, Formulaires).</li>
    <li><strong>Gestion de l'État :</strong> L'état de l'application est géré localement (par composant ou via React Context) pour les données affichées et les interactions utilisateur.</li>
    <li><strong>Moteur IA :</strong> Le module de logique intelligente s'exécute uniquement sur l'appareil (via des algorithmes JS ou potentiellement un modèle léger) et interagit avec les données locales pour les suggestions.</li>
  </ul>
</div>

## 💾 Persistence Locale (SQLite/AsyncStorage)

<div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 my-8">
  <p class="text-sm dark:text-white/70 text-slate-600 leading-relaxed mb-4">
    Pour garantir l'accès aux données des événements même sans connexion Internet, une solution de **persistence locale** a été mise en œuvre. Cela assure une expérience utilisateur rapide et fiable.
  </p>
  <ul class="list-disc list-outside space-y-2 pl-5 text-sm dark:text-white/70 text-slate-600">
    <li><strong>Choix de la DB :</strong> Utilisation de SQLite (via l'API Expo) ou d'AsyncStorage pour la persistance des événements et des configurations utilisateur.</li>
    <li><strong>Logique CRUD :</strong> Implémentation des fonctions de Création, Lecture, Mise à jour et Suppression des événements directement sur le *store* local.</li>
    <li><strong>Data Layer :</strong> Séparation de la couche d'accès aux données pour que les composants UI n'interagissent qu'avec les fonctions de haut niveau (ex: `EventService.addEvent`).</li>
    <li><strong>Schéma de données :</strong> Définition d'un schéma structuré pour les objets `Event` et `Task` afin de faciliter la détection de conflits par le Moteur IA.</li>
  </ul>
</div>

## 📝 Formulaires et Ergonomie

<div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 my-8">
  <p class="text-sm dark:text-white/70 text-slate-600 leading-relaxed mb-4">
    La qualité de l'expérience utilisateur (UX) a été une priorité, notamment pour la création et la modification d'événements, qui nécessitent une saisie structurée et une **validation robuste**.
  </p>
  <ul class="list-disc list-outside space-y-2 pl-5 text-sm dark:text-white/70 text-slate-600">
    <li><strong>Formik :</strong> Utilisation de Formik pour gérer l'état du formulaire, les valeurs, les erreurs et la soumission sans écrire de code boilerplate.</li>
    <li><strong>Yup :</strong> Mise en œuvre de la bibliothèque Yup pour la validation du schéma. Cela garantit que les dates et heures saisies sont valides avant d'être sauvegardées.</li>
    <li><strong>Accessibilité mobile :</strong> Utilisation de composants optimisés pour la saisie tactile et les sélecteurs de date/heure natifs de l'OS mobile.</li>
  </ul>
</div>

## 🎓 Compétences démontrées

<div class="skills-showcase space-y-6 my-8">
  
  <div class="skill-category dark:bg-gradient-to-r dark:from-indigo-900/30 dark:to-purple-900/30 bg-gradient-to-r from-indigo-50 to-purple-50 border dark:border-indigo-500/30 border-indigo-300 rounded-2xl p-6 hover:scale-[1.02] transition-all duration-300">
    <div class="flex items-center gap-3 mb-4">
      <span class="text-3xl">⚛️</span>
      <h3 class="text-xl font-bold dark:text-white text-slate-900">Développement Mobile (React Native)</h3>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Framework Mobile</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Maîtrise de React Native et de ses composants natifs.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Workflow Expo</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Utilisation d'Expo pour le *bundling* et les tests rapides.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Gestion de la Navigation</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Implémentation de React Navigation (routing par piles).</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Persistence Asynchrone</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Utilisation de SQLite/AsyncStorage pour le mode hors ligne.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="skill-category dark:bg-gradient-to-r dark:from-indigo-900/30 dark:to-purple-900/30 bg-gradient-to-r from-indigo-50 to-purple-50 border dark:border-indigo-500/30 border-indigo-300 rounded-2xl p-6 hover:scale-[1.02] transition-all duration-300">
    <div class="flex items-center gap-3 mb-4">
      <span class="text-3xl">🧠</span>
      <h3 class="text-xl font-bold dark:text-white text-slate-900">Logique Applicative & IA</h3>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Algorithmes d'ordonnancement</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Détection de conflits d'horaire et proposition de solutions.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Validation de Schéma</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Utilisation de Yup pour la validation des données du formulaire.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Formulaires Avancés (Formik)</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Gestion de l'état des formulaires complexes de création d'événement.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Data Modeling</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Structuration des objets `Event` et `Task` pour la base de données.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="skill-category dark:bg-gradient-to-r dark:from-indigo-900/30 dark:to-purple-900/30 bg-gradient-to-r from-indigo-50 to-purple-50 border dark:border-indigo-500/30 border-indigo-300 rounded-2xl p-6 hover:scale-[1.02] transition-all duration-300">
    <div class="flex items-center gap-3 mb-4">
      <span class="text-3xl">🤝</span>
      <h3 class="text-xl font-bold dark:text-white text-slate-900">Gestion de Projet (Groupe)</h3>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Coordination d'équipe</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Travail collaboratif sur un projet long (5 membres).</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Versionnement (Git)</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Gestion des branches, *pull requests* et résolution de conflits.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Méthodes Agiles légères</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Planification des sprints et suivi de l'avancement du projet annuel.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Prototypage rapide (Expo)</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Utilisation de l'outil Expo Go pour les démos rapides en classe.</div>
        </div>
      </div>
    </div>
  </div>
</div>

## 📚 Ressources & Documentation

<div class="documentation-grid grid grid-cols-1 md:grid-cols-2 gap-6 my-8">
  
  <div class="doc-card dark:bg-gradient-to-br dark:from-slate-900/50 dark:to-slate-800/50 bg-gradient-to-br from-slate-50 to-slate-100 border dark:border-white/10 border-slate-300 rounded-2xl p-6 hover:scale-[1.02] transition-all duration-300 cursor-pointer" data-doc-type="details">
    <div class="flex items-center gap-3 mb-4">
      <span class="text-3xl">📖</span>
      <h3 class="text-lg font-bold dark:text-white text-slate-900">Documentation complète</h3>
    </div>
    <ul class="space-y-3">
      <li class="flex items-start gap-2">
        <span class="text-blue-500">▸</span>
        <span class="dark:text-white/70 text-slate-600">Détails sur les algorithmes de détection de conflit</span>
      </li>
      <li class="flex items-start gap-2">
        <span class="text-blue-500">▸</span>
        <span class="dark:text-white/70 text-slate-600">Schéma des données SQLite / AsyncStorage</span>
      </li>
      <li class="flex items-start gap-2">
        <span class="text-blue-500">▸</span>
        <span class="dark:text-white/70 text-slate-600">Procédures d'installation et de build Expo</span>
      </li>
      <li class="flex items-start gap-2">
        <span class="text-blue-500">▸</span>
        <span class="dark:text-white/70 text-slate-600">Rapport de projet et répartition des tâches (Git)</span>
      </li>
    </ul>
    <div class="mt-4 text-center">
      <span class="text-sm dark:text-blue-400 text-blue-600 font-semibold">→ Voir les détails techniques</span>
    </div>
  </div>

  <div class="doc-card dark:bg-gradient-to-br dark:from-purple-900/30 dark:to-indigo-900/30 bg-gradient-to-br from-purple-50 to-indigo-50 border dark:border-purple-500/30 border-purple-300 rounded-2xl p-6 hover:scale-[1.02] transition-all duration-300 cursor-pointer" data-doc-type="architecture">
    <div class="flex items-center gap-3 mb-4">
      <span class="text-3xl">🗺️</span>
      <h3 class="text-lg font-bold dark:text-white text-slate-900">Diagramme interactif</h3>
    </div>
    <p class="dark:text-white/70 text-slate-600 mb-4">Visualisation complète de l'architecture avec tooltips détaillés pour chaque composant.</p>
    <div class="flex flex-wrap gap-2 mb-4">
      <span class="px-3 py-1 dark:bg-blue-500/20 bg-blue-200 dark:text-blue-300 text-blue-700 rounded-full text-xs">React Native</span>
      <span class="px-3 py-1 dark:bg-red-500/20 bg-red-200 dark:text-red-300 text-red-700 rounded-full text-xs">IA / Logique</span>
      <span class="px-3 py-1 dark:bg-purple-500/20 bg-purple-200 dark:text-purple-300 text-purple-700 rounded-full text-xs">Persistence</span>
      <span class="px-3 py-1 dark:bg-green-500/20 bg-green-200 dark:text-green-300 text-green-700 rounded-full text-xs">Formulaires</span>
    </div>
    <div class="text-center">
      <span class="text-sm dark:text-purple-400 text-purple-600 font-semibold">→ Voir l'architecture</span>
    </div>
  </div>

</div>

<script is:inline>
  document.addEventListener('DOMContentLoaded', function() {
    const docCards = document.querySelectorAll('[data-doc-type]');
    docCards.forEach(card => {
      card.addEventListener('click', function() {
        const type = this.getAttribute('data-doc-type');
        const tabButton = document.querySelector(`[data-tab="${type}"]`);
        if (tabButton) {
          tabButton.click();
        }
      });
    });
  });
</script>

---

**Archivé** | **Application Mobile** | **Projet Académique (ESGI)**
