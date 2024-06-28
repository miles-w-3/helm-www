---
title: "Helm Search Repo"
---

## helm search repo

Rechercher par mot clé dans les répertoires de charts

### Synopsis

La recherche parcourt tous les référentiels configurés sur le système et recherche les correspondances.. La recherche dans ces répertoires utilise les métadonnées stockées sur le système.

Il affichera les dernières versions stables des charts trouvés. Si vous spécifiez l'argument `--devel`, cela inclura des versions préliminaires.
Si vous voulez faire une recherche en utilisant une contrainte de version, utilisez l'argument `--version`.

Examples :

    # Recherchez les versions stables correspondant au mot-clé "nginx"
    $ helm search repo nginx

    # Recherchez les versions correspondant au mot-clé "nginx", incluant les versions préliminaires
    $ helm search repo nginx --devel

    # Recherchez les dernières versions stables pour nginx-ingress avec une version majeur de 1
    $ helm search repo nginx-ingress --version ^1.0.0

Les répertoires sont gérés avec la commande `helm repo`.


```
helm search repo [keyword] [flags]
```

### Options

```
      --devel                Utiliser également les version de développement (alpha, beta, et versions candidates). Équivalent à version '>0.0.0-0'. Si --version est fixé, cela sera ignoré
      --fail-on-no-result    La recherche échoue si pas de résultat trouvé
  -h, --help                 Aide pour la commande repo
      --max-col-width uint   Largeur maximum de colonne pour la table de sortie (par défaut 50)
  -o, --output format        Affiche la sortie dans le format spécifié. Valeurs autorisées : table, json, yaml (par défaut table)
  -r, --regexp               Utiliser des expressions régulières pour rechercher dans les réportoires que vous avez ajoutés
      --version string       Utiliser une contrainte de version sémantique sur les répertoires que vous avez ajoutés
  -l, --versions             Affiche la longue liste, avec chaque version de chaque chart sur sa propre ligne, pour les répertoires que vous avez ajoutés
```

### Options héritées des commandes parents

```
      --burst-limit int                 Limite coté client de la bande passante (par défaut 100)
      --debug                           Active la sortie détaillée
      --kube-apiserver string           L'adresse et le port API du serveur Kubernetes
      --kube-as-group stringArray       Groupe à utiliser pour l'opération, cet argument peut être répété pour spécifier plusieurs groupes
      --kube-as-user string             Nom d'utilisateur à utiliser pour l'operation
      --kube-ca-file string             Le fichier de l'autorité de certification pour la connexion à l'API Kubernetes
      --kube-context string             Nom du contexte kubeconfig à utiliser
      --kube-insecure-skip-tls-verify   Si true, la validité du certificat du serveur API Kubernetes ne sera pas vérifiée. Cela fera les connexions HTTPS non sûres
      --kube-tls-server-name string     Nom du serveur utilisé pour la validation du certificat du serveur API Kubernetes. S'il n'est pas fourni, le nom de la machine cliente utilisée pour contacter le serveur sera utilisé
      --kube-token string               Jeton utilisé pour l'authentification
      --kubeconfig string               Chemin du fichier de configuration kubeconfig
  -n, --namespace string                Namespace à utilisé pour la requête
	  --qps float32                     Requêtes par seconde utilisées lors de la communication avec l'API Kubernetes, sans compter le bursting
      --registry-config string          Chemin vers le fichier de configuration du registre (par défaut "~/.config/helm/registry/config.json")
      --repository-cache string         Chemin vers le fichier contenant les index du répertoire mis en cache (par défaut "~/.cache/helm/repository")
      --repository-config string        Chemin vers le fichier contenant les noms et URLs des répertoires (par défaut "~/.config/helm/repositories.yaml")
```

### Voir également

* [helm search](helm_search.md) - Recherche par mot clé dans les charts
