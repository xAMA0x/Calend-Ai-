---
title: "Calend-Ai"
description: "Application mobile de gestion pour étudiants (devoirs, calendrier, notes) intégrant l'API non documentée de MyGES."
date: "2024-04-24"
tags: ["javascript","react-native","mobile","api-reverse","myges"]
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
  - name: "API MyGES (Reverse Engineering)"
    category: "network"
    icon: "🔑"
  - name: "SQLite"
    category: "database"
    icon: "💾"
  - name: "Logique IA (Suggestion)"
    category: "tool"
    icon: "🧠"

# Architecture du projet
architecture:
  overview: "L'architecture est une application mobile monolithique (front-end seul) typique de React Native/Expo. Le cœur du projet est la couche d'accès aux données : un module a été développé pour interagir avec l'API non documentée de MyGES. Les données critiques (notes, calendrier) sont synchronisées et stockées localement via SQLite pour une utilisation hors ligne, tandis que l'interface React Navigation gère la structure des vues (Calendrier natif, Vue Notes, etc.)."
  components:
    - "Cœur React Native (JavaScript) : Gère le rendu de l'UI, le cycle de vie des composants et la logique d'affichage."
    - "Module API MyGES (Reverse Engineering) : Le composant critique pour l'authentification et l'extraction des données (notes, absences, devoirs) sans documentation officielle."
    - "Persistence Locale (SQLite) : Stocke les données des événements, des tâches et des notes directement sur l'appareil pour garantir l'accès hors ligne et la rapidité."
    - "React Navigation (Routing) : Gère la navigation entre les écrans (ex: Écran Calendrier, Écran Tâches, Écran Configuration) via un système de piles."
    - "Logique IA / Moteur de Suggestion : Module central pour l'aspect intelligent du projet (détection des conflits d'horaire et proposition de tâches)."

# Diagrammes d'architecture (optionnel)
diagrams:
  - path: "https://raw.githubusercontent.com/xAMA0x/Calend-Ai-/main/.portfolio/diagrams/calend-ai-architecture.svg"
    title: "Architecture Mobile et Flux API MyGES"
    description: "Flux de données et séparation des modules dans l'application mobile."

# URLs et liens
demo_url: ""
demo_label: ""
github_url: "https://github.com/xAMA0x/Calend-Ai-"
---

## 🎯 Vue d'ensemble

<div class="overview-hero dark:bg-gradient-to-br dark:from-accent/10 dark:to-purple-900/10 bg-gradient-to-br from-indigo-50 to-purple-50 border dark:border-accent/20 border-indigo-200 rounded-2xl p-8 my-8 shadow-lg">
  <p class="text-lg dark:text-white/90 text-slate-700 leading-relaxed mb-6">
    <strong>Calend-Ai</strong> est une application de gestion critique pour les étudiants de l'Eductive, conçue pour un accès <strong>centralisé</strong> et **mobile** à leurs données académiques. Le défi technique principal fut le **Reverse Engineering de l'API MyGES** pour extraire les notes, absences et devoirs. Ce projet de groupe ESGI démontre une expertise à la fois en développement **React Native** et en **programmation réseau de bas niveau** face à des systèmes non documentés.
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
      <div class="stat-label text-sm dark:text-white/60 text-slate-600">API Reverse Engineered</div>
    </div>
  </div>
</div>

### Objectifs du projet

<div class="objectives-grid grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 my-8">
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      🔑
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Reverse Engineering API MyGES
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Découvrir et implémenter une couche de communication stable avec l'API MyGES pour pallier l'absence de documentation officielle.
    </p>
  </div>
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      📅
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Intégration Calendrier Natif
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Synchroniser les emplois du temps académiques avec les applications natives iOS et Android (Google Calendar/Apple Calendar).
    </p>
  </div>
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      💯
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Accès Mobile aux Notes & Absences
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Créer un dashboard pour afficher les notes, les absences et les devoirs directement sur le téléphone.
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
      Développer une logique algorithmique pour détecter les chevauchements et proposer des ajustements d'horaires et de tâches.
    </p>
  </div>
  <div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 hover:scale-105 transition-all duration-300 hover:shadow-xl">
    <div class="icon-wrapper text-4xl mb-4 flex items-center justify-center w-16 h-16 rounded-full dark:bg-white/10 bg-slate-100 mx-auto">
      🤝
    </div>
    <h3 class="text-lg font-semibold mb-2 dark:text-white text-slate-900 text-center">
      Projet d'Équipe (5 Membres)
    </h3>
    <p class="text-sm dark:text-white/70 text-slate-600 text-center leading-relaxed">
      Assurer la coordination technique, la gestion des dépendances (NPM) et le versionnement Git d'une application mobile complexe.
    </p>
  </div>
</div>

## 🔑 Reverse Engineering de l'API MyGES

<div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 my-8">
  <p class="text-sm dark:text-white/70 text-slate-600 leading-relaxed mb-4">
    C'est le défi central. L'absence de documentation officielle de MyGES a nécessité une approche de **Reverse Engineering** des communications réseau pour implémenter un module de connexion et d'extraction de données fiable.
  </p>
  <ul class="list-disc list-outside space-y-2 pl-5 text-sm dark:text-white/70 text-slate-600">
    <li><strong>Analyse de Protocole :</strong> Utilisation d'outils (ex: Proxies HTTP) pour intercepter et analyser les requêtes faites par le site web ou l'application MyGES officielle.</li>
    <li><strong>Implémentation d'Authentification :</strong> Reproduction du flux d'authentification (souvent basé sur des tokens ou des sessions cookies) pour obtenir l'accès aux données utilisateur.</li>
    <li><strong>Extraction des Endpoints :</strong> Identification des URLs spécifiques pour récupérer les notes, les absences et l'emploi du temps (souvent au format JSON).</li>
    <li><strong>Gestion des erreurs :</strong> Implémentation de mécanismes de *retry* et de gestion des erreurs pour maintenir la synchronisation stable malgré les changements potentiels de l'API non documentée.</li>
  </ul>
</div>

## 📅 Logique Métier & Synchronisation

<div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 my-8">
  <p class="text-sm dark:text-white/70 text-slate-600 leading-relaxed mb-4">
    Le cœur de l'application gère la **synchronisation** des données académiques avec la logique de planification locale de l'utilisateur.
  </p>
  <ul class="list-disc list-outside space-y-2 pl-5 text-sm dark:text-white/70 text-slate-600">
    <li><strong>Synchronisation Bidi :</strong> L'application gère la synchronisation de la DB locale (SQLite) avec l'API MyGES (extraction) et les calendriers natifs (export des événements).</li>
    <li><strong>Logique IA (Suggestion) :</strong> Algorithmes JavaScript pour analyser l'emploi du temps récupéré de MyGES et les devoirs/tâches locaux afin de suggérer les meilleurs créneaux.</li>
    <li><strong>Notification :</strong> Mise en œuvre des notifications mobiles pour alerter les étudiants des devoirs à venir ou des changements d'emploi du temps.</li>
  </ul>
</div>

## ⚛️ Stack Mobile (React Native / Expo)

<div class="objective-card dark:bg-white/5 bg-white/80 backdrop-blur-md border dark:border-white/10 border-slate-200 rounded-xl p-6 my-8">
  <p class="text-sm dark:text-white/70 text-slate-600 leading-relaxed mb-4">
    Le développement est entièrement basé sur l'écosystème **React Native**, garantissant une application native unique pour iOS et Android, avec une interface réactive.
  </p>
  <ul class="list-disc list-outside space-y-2 pl-5 text-sm dark:text-white/70 text-slate-600">
    <li><strong>Développement Cross-Plateforme :</strong> Utilisation de React Native pour le développement simultané sur iOS et Android à partir d'une seule base de code JS.</li>
    <li><strong>Workflow Expo :</strong> Utilisation d'Expo pour la simplification du build, du *bundling* et des tests en temps réel (via l'application Expo Go).</li>
    <li><strong>Gestion de l'État et du Routing :</strong> Mise en œuvre de la gestion de l'état (Context API ou Hooks) et de `React Navigation` pour le routing entre les différents dashboards (Notes, Calendrier).</li>
  </ul>
</div>

## 🎓 Compétences démontrées

<div class="skills-showcase space-y-6 my-8">
  
  <div class="skill-category dark:bg-gradient-to-r dark:from-indigo-900/30 dark:to-purple-900/30 bg-gradient-to-r from-indigo-50 to-purple-50 border dark:border-indigo-500/30 border-indigo-300 rounded-2xl p-6 hover:scale-[1.02] transition-all duration-300">
    <div class="flex items-center gap-3 mb-4">
      <span class="text-3xl">🔑</span>
      <h3 class="text-xl font-bold dark:text-white text-slate-900">Programmation Réseau & API</h3>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Reverse Engineering API</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Analyse de requêtes pour API MyGES sans documentation.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Gestion de l'Authentification</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Reproduction du flux d'authentification MyGES (tokens/cookies).</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Synchronisation des Données</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Logique pour l'extraction et le rafraîchissement des notes/calendrier.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Persistence Hors Ligne</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Utilisation de SQLite pour le stockage sécurisé des données académiques.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="skill-category dark:bg-gradient-to-r dark:from-indigo-900/30 dark:to-purple-900/30 bg-gradient-to-r from-indigo-50 to-purple-50 border dark:border-indigo-500/30 border-indigo-300 rounded-2xl p-6 hover:scale-[1.02] transition-all duration-300">
    <div class="flex items-center gap-3 mb-4">
      <span class="text-3xl">⚛️</span>
      <h3 class="text-xl font-bold dark:text-white text-slate-900">Développement Mobile (Front-end)</h3>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Framework Cross-Plateforme</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Développement natif unique avec React Native/Expo (iOS/Android).</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Intégration Calendrier Natif</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Export des événements vers les calendriers natifs de l'OS.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Gestion de l'État et du Routing</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Utilisation des Hooks et de React Navigation pour le flux utilisateur.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">UX/UI Mobile</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Conception des dashboards (Notes, Absences) pour petit écran.</div>
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
          <div class="text-xs dark:text-white/60 text-slate-600">Travail collaboratif (5 membres) sur une base de code complexe.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Planification (ESGI)</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Planification et suivi des tâches du projet annuel de 2e année.</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Gestion des Dépendances</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Gestion et mise à jour du *package.json* (NPM).</div>
        </div>
      </div>
      <div class="skill-item flex items-start gap-2 dark:bg-white/5 bg-white/50 rounded-lg p-3">
        <span class="text-green-500 font-bold text-lg">✓</span>
        <div>
          <div class="font-semibold dark:text-white text-slate-900">Logique d'auto-correction</div>
          <div class="text-xs dark:text-white/60 text-slate-600">Gestion des erreurs de parsing suite à des changements API externes.</div>
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
        <span class="dark:text-white/70 text-slate-600">Rapport d'analyse du protocole MyGES (Reverse Engineering)</span>
      </li>
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
      <span class="px-3 py-1 dark:bg-blue-500/20 bg-blue-200 dark:text-blue-300 text-blue-700 rounded-full text-xs">API Reverse</span>
      <span class="px-3 py-1 dark:bg-red-500/20 bg-red-200 dark:text-red-300 text-red-700 rounded-full text-xs">Logique IA</span>
      <span class="px-3 py-1 dark:bg-purple-500/20 bg-purple-200 dark:text-purple-300 text-purple-700 rounded-full text-xs">Persistence</span>
      <span class="px-3 py-1 dark:bg-green-500/20 bg-green-200 dark:text-green-300 text-green-700 rounded-full text-xs">React Native</span>
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
