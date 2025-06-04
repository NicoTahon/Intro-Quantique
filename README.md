# Atelier Qiskit avec IBM Quantum

Ce projet présente un exemple simple d'utilisation du module **Qiskit Runtime** d'IBM pour soumettre un circuit quantique à un backend quantique réel, via le **Sampler V2**.

## 📋 Prérequis

Avant d'exécuter le script, assure-toi d'avoir :

- Un compte IBM Quantum : [https://quantum.ibm.com](https://quantum.ibm.com)
- Une **clé API** IBM Quantum disponible sur ton compte
- Un fichier `.env` à la racine du projet contenant :

```
IQP_API_TOKEN=your_ibm_quantum_api_token_here
```

- Python 3.8 ou supérieur
- Les packages suivants installés :

```bash
pip install qiskit qiskit-ibm-runtime python-dotenv
```

## 🚀 Description du code

Le script fait les étapes suivantes :

1. Charge le token API depuis un fichier `.env`
2. Enregistre ce token dans la configuration Qiskit
3. Crée un circuit quantique simple de 2 qubits avec une mesure
4. Recherche le backend réel le moins occupé
5. Soumet le circuit au backend via le **Sampler V2**
6. Affiche l'identifiant du job et le résultat

## 📄 Exemple de sortie

```
job id: cj1k0abc123xyz
SamplerResult(quasi_dists=[...])
```

## 🧠 Remarques

- Le circuit utilisé est très simple (aucune porte appliquée) ; il peut être modifié pour tester des opérations plus complexes.
- L'utilisation du `SamplerV2` est adaptée pour estimer la distribution de sortie des circuits.
- Le backend sélectionné est un **véritable ordinateur quantique**, pas un simulateur.

## 🛡️ Sécurité

Ne publie **jamais** ta clé API (`IQP_API_TOKEN`) sur un dépôt public.

## 📚 Ressources utiles

- [Documentation Qiskit Runtime](https://qiskit.org/documentation/partners/qiskit_ibm_runtime/)
- [Créer un compte IBM Quantum](https://quantum.ibm.com)
- [API Reference Qiskit Runtime](https://docs.quantum.ibm.com/api/qiskit-ibm-runtime)
