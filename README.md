# James Assistant 🤖

**James** est un assistant personnel intelligent qui tourne localement sur ton ordinateur. Il t'aide à organiser ton travail, optimiser ta productivité, structurer tes recherches et apprendre l'intelligence artificielle.

## 🎯 Objectif

James est ton assistant personnel :
- **Maison** : organisation quotidienne, routines, tâches personnelles
- **Business** : productivité, projets, décisions, stratégie
- **IA** : apprentissage, concepts, ressources, parcours structuré

## ✨ Fonctionnalités

✅ Assistant conversationnel local (fonctionne sans internet)
✅ Gestion de projets et tâches
✅ Organisation du temps et priorités
✅ Recherche structurée et synthèse
✅ Accompagnement apprentissage IA
✅ Mémoire persistante (contexte, historique)
✅ Suggestions proactives
✅ Démarrage automatique au lancement du PC

## 📋 Table des matières

- [Installation](#installation)
- [Démarrage rapide](#démarrage-rapide)
- [Configuration](#configuration)
- [Utilisation](#utilisation)
- [Architecture](#architecture)
- [Troubleshooting](#troubleshooting)

## 🚀 Installation

### Prérequis

- Python 3.9+
- pip
- Un modèle LLM local (Ollama, LM Studio ou API)

### Étape 1 : Cloner le repo

```bash
git clone https://github.com/plus6stephane/jarvis-assistant-skill.git
cd jarvis-assistant-skill
```

### Étape 2 : Installer les dépendances

```bash
pip install -r requirements.txt
```

### Étape 3 : Configurer James

```bash
cp config.example.json config.json
# Édite config.json avec tes paramètres
```

### Étape 4 : Tester le lancement

```bash
python james.py
```

## ⚡ Démarrage rapide

### Lancer James en mode CLI

```bash
python james.py
```

### Lui parler

```
James> Aide-moi à prioriser ma semaine
James> Je veux apprendre le machine learning, par où commencer ?
James> Organise mes tâches de travail
James> Cherche des infos sur les LLMs
```

### Quitter

```
James> exit
```

## ⚙️ Configuration

Édite `config.json` :

```json
{
  "name": "James",
  "model": "mistral",
  "api_type": "ollama",
  "api_url": "http://localhost:11434",
  "temperature": 0.7,
  "max_tokens": 2048,
  "language": "fr",
  "memory_enabled": true,
  "auto_start": true,
  "log_file": "james.log"
}
```

**Options API** :
- `ollama` : local, rapide, recommandé
- `lm_studio` : local, très flexible
- `openai` : cloud (nécessite clé API)

## 📖 Utilisation

### Modes de James

#### 1. Mode Productivité
```
James> Je veux être plus productif cette semaine
→ James propose une routine, priorise tes tâches, suggère des optimisations
```

#### 2. Mode Recherche
```
James> Recherche des infos sur la programmation orientée objet
→ James résume les concepts clés, propose des ressources, synthétise
```

#### 3. Mode Apprentissage IA
```
James> Je veux apprendre l'IA, par où commencer ?
→ James crée un parcours structuré, explique, propose des exercices
```

#### 4. Mode Gestion
```
James> Organise ma semaine, j'ai 10 tâches
→ James priorise, crée un calendrier, identifie les dépendances
```

### Commandes spéciales

```
/save [nom]       - Sauvegarde la conversation actuelle
/load [nom]       - Charge une conversation précédente
/reset            - Réinitialise la mémoire
/status           - Affiche l'état de James
/help             - Affiche l'aide
/exit             - Quitte James
```

## 🏗️ Architecture

```
jarvis-assistant-skill/
├── james.py                 # Point d'entrée principal
├── config.json              # Configuration
├── requirements.txt         # Dépendances
├── james/
│   ├── __init__.py
│   ├── core.py             # Moteur principal
│   ├── memory.py           # Système de mémoire
│   ├── prompts.py          # Prompts et instructions
│   ├── modes.py            # Modes de fonctionnement
│   ├── utils.py            # Utilitaires
│   └── api/
│       ├── ollama.py       # Intégration Ollama
│       ├── lm_studio.py    # Intégration LM Studio
│       └── openai.py       # Intégration OpenAI
├── data/
│   ├── conversations/      # Historique des conversations
│   ├── memory.json         # Mémoire persistante
│   └── projects/           # Gestion de projets
├── scripts/
│   ├── install.py          # Script d'installation
│   ├── autostart_windows.py # Démarrage auto (Windows)
│   ├── autostart_mac.py    # Démarrage auto (Mac)
│   ├── autostart_linux.py  # Démarrage auto (Linux)
│   └── launch_at_startup.py
└── docs/
    ├── INSTALL.md          # Guide d'installation détaillé
    ├── USAGE.md            # Guide d'utilisation
    └── API.md              # Documentation de l'API
```

## 🔧 Démarrage automatique

### Windows

```bash
python scripts/autostart_windows.py
```

### Mac

```bash
python scripts/autostart_mac.py
```

### Linux

```bash
python scripts/autostart_linux.py
```

## 🤝 Contribuer

Les contributions sont bienvenues ! N'hésite pas à ouvrir une issue ou un PR.

## 📝 Licence

MIT License - voir [LICENSE](LICENSE)

## 📞 Support

Pour toute question ou problème :
- Ouvre une [issue](https://github.com/plus6stephane/jarvis-assistant-skill/issues)
- Consulte la [documentation](docs/)
- Envoie un message

---

**James** — Ton assistant personnel, toujours disponible, prêt à t'aider. 🚀
