# Backend

## Supabase

https://supabase.com/docs/guides/cli/getting-started

```
supabase init
```

# Hosting

## Supabase

https://supabase.com/docs/guides/self-hosting

fork du projet

Repository settings - Fork behaviour
For my own purposes


```
git clone --depth 1 git@github.com:medina474/sae5-hosting.git
```

créer une branche

cd sae5-hosting/docker
cp .env.example .env

Mettre à jour le fichier .env

```toml
STUDIO_DEFAULT_ORGANIZATION=IUT de Saint-Dié
STUDIO_DEFAULT_PROJECT=SAE5
```

Générer un JWT secret (46 caract Aa9)

Sur la page générer ANON_KEY et SERVICE_KEY avec ce secret les recopier dans le fichier .env

```toml
DASHBOARD_USERNAME=votre email
DASHBOARD_PASSWORD=votre mot de passe
```

docker compose pull

docker compose up -d

### Override

créer un fichier compose.override.yml

docker compose restart
