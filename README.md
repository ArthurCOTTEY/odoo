# Installation Odoo Docker

## 1. Copier le fichier d’environnement

```bash
cp .env.example .env
2. Modifier le fichier .env
POSTGRES_USER=u_482916
POSTGRES_DB=db_739284
POSTGRES_PASSWORD=mot_de_passe_securise
3. Initialiser Odoo puis démarrer
docker compose run --rm web odoo -d db_739284 -i base --stop-after-init && docker compose up -d

Remplacer db_739284 par la valeur de POSTGRES_DB.

4. Accéder à Odoo
http://IP_DU_SERVEUR:8069
5. Démarrage normal
docker compose up -d
6. Arrêter Odoo
docker compose down
7. Réinitialiser complètement

Attention : supprime toutes les données Odoo et PostgreSQL.

docker compose down -v