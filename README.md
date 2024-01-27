# Développement

## Supabase

https://supabase.com/docs/guides/cli/getting-started
https://medium.com/@igor.mytyuk/supabase-self-hosted-deploy-475718fe906f

```shell-session
git init
supabase init
supabase start
```

http://localhost:54323/

```shell-session
supabase migration new jardins
```

le code sql puis

```shell-session
supabase migration up
```

supabase db push --db-url postgresql://postgres:your-super-secret-and-long-postgres-password@localhost:5432/postgres

# Recette

## Supabase

https://supabase.com/docs/guides/self-hosting

fork du projet dans GitHub

```
git clone --depth 1 git@github.com:medina474/sae5-hosting.git
```

Ajouter le projet dans GitHub Desktop

Repository settings - Fork behaviour
For my own purposes

créer une branche

### Personnaliser l'installation

cd sae5-hosting/docker
cp .env.example .env

Mettre à jour le fichier .env

```ini
STUDIO_DEFAULT_ORGANIZATION=IUT de Saint-Dié
STUDIO_DEFAULT_PROJECT=SAE5
```

Générer un JWT secret (46 caract Aa9)

Sur la page générer ANON_KEY et SERVICE_KEY avec ce secret les recopier dans le fichier .env

```ini
DASHBOARD_USERNAME=votre email
DASHBOARD_PASSWORD=votre mot de passe
```

```shell-session
docker compose pull

docker compose up -d
```

### Override

créer un fichier compose.override.yml

docker compose restart

# Production

https://supabase.com/docs/guides/cli/managing-environments

```shell-session
supabase login
supabase link --project-ref $PROJECT_ID
```