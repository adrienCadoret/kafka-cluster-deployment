# Kafka deployment

Ce playbook permet de déployer la documentation VIF sur un serveur.

Pour le moment le mode HA n'est pas géré.

Toutes les données statiques (repositories à génerer) sont initialisées par ce playbook via les variables:

* antora_sources

## Utilisation du playbook
Lancement de l'installation

``` bash
ansible-playbook -i inventory.yml doc-deployment-playbook.yml
```

Ce playbook utilise des rôles `ansible-galaxy`.

Il est donc nécessaire de télécharger les rôles avant de lancer le playbook:

``` bash
ansible-galaxy install -p roles -r requirements.yml
```
