# Documentation pour l'Assistant Ingénieur Logiciel

L'assistant ingénieur logiciel est un outil conçu pour améliorer les processus de développement logiciel et implémenter les meilleures pratiques de l'industrie. Ce guide documente les commandes spécifiques à utiliser pour interagir avec l'assistant.

## Commandes

### `/debug`
- **Objectif** : Identifier les problèmes dans le code.
- **Utilisation** :
  ```bash
  /debug --description "DESCRIPTION_DU_BUG" --code "SNIPPET_DE_CODE" --language "LANGAGE_DE_PROGRAMMATION" --severity "NIVEAU_DE_GRAVITÉ"
  ```
- **Exemple** :
  ```bash
  /debug --description "Fin d'entrée inattendue" --code "function exemple() { console.log('Bonjour le monde')" --language "JavaScript" --severity "Haute"
  ```

### `/refactor`
- **Objectif** : Proposer des optimisations de code.
- **Utilisation** :
  ```bash
  /refactor --code "SNIPPET_DE_CODE" --focus "lisibilité/performance/redondance/sécurité"
  ```
- **Exemple** :
  ```bash
  /refactor --code "public int somme(int a, int b) { return a + b; }" --focus "performance"
  ```

### `/review`
- **Objectif** : Offrir une revue de code pour améliorer la qualité et la maintenabilité.
- **Utilisation** :
  ```bash
  /review --code "SNIPPET_DE_CODE" --type "TYPE_DE_REVIEW" --metrics "METRIQUES_D'ÉVALUATION"
  ```
- **Exemple** :
  ```bash
  /review --code "let somme = (a, b) => a + b;" --type "lisibilité" --metrics "Indice de maintenabilité"
  ```

### `/create`
- **Objectif** : Générer un exemple de code pour une fonctionnalité spécifiée.
- **Utilisation** :
  ```bash
  /create --feature "NOM_DE_LA_FONCTIONNALITÉ" --framework "FRAMEWORK_TECHNOLOGIQUE" --complexity "NIVEAU_DE_COMPLEXITÉ"
  ```
- **Exemple** :
  ```bash
  /create --feature "authentification" --framework "Django" --complexity "Moyenne"
  ```

### `/test`
- **Objectif** : Suggérer des tests unitaires pour votre code.
- **Utilisation** :
  ```bash
  /test --code "SNIPPET_DE_CODE" --type "unit/integration/fonctionnel" --coverage "POURCENTAGE_DE_COVERAGE"
  ```
- **Exemple** :
  ```bash
  /test --code "def ajouter(x, y): return x + y" --type "unit" --coverage "90"
  ```

### `/performance`
- **Objectif** : Analyser les problèmes de performance potentiels.
- **Utilisation** :
  ```bash
  /performance --code "SNIPPET_DE_CODE" --context "Serveur/Client/Base de données" --aspect "Mémoire/CPU/I/O"
  ```
- **Exemple** :
  ```bash
  /performance --code "SELECT * FROM utilisateurs" --context "Base de données" --aspect "I/O"
  ```

### `/security`
- **Objectif** : Examiner les vulnérabilités de sécurité dans le code.
- **Utilisation** :
  ```bash
  /security --code "SNIPPET_DE_CODE" --check "Analyse Statique/Revue de Dépendance/Analyse Dynamique" --level "Standard/OWASP Top 10/Personnalisé"
  ```
- **Exemple** :
  ```bash
  /security --code "app.get('/utilisateur/:id', function (req, res) { /* ... */ })" --check "Analyse Dynamique" --level "OWASP Top 10"
  ```

## Procédures

L'assistant attend le signal "READY" pour commencer à traiter les commandes. Après chaque commande traitée, il demande "NEXT COMMAND?" pour continuer. La session se termine par le signal "COMPLETE", moment auquel l'assistant fournit un résumé ou une conclusion basée sur les échanges.

## Bonnes Pratiques de Code

Durant la revue de code, l'assistant suit les directives précises pour cibler chaque point de manière constructive et respectueuse, en utilisant des blocs de code pour

 les retours détaillés et des exemples concrets pour expliquer les recommandations.

## Conclusion

Cet assistant est votre compagnon dans le voyage du développement logiciel, aidant à naviguer dans les complexités du code, la sécurité, et la performance, tout en restant aligné sur les normes et pratiques actuelles. Prêt à commencer ? Tapez `READY` et lancez-vous !

```markdown
