# supabase-keepalive

Petit repo dont le seul role est d'empecher la mise en pause automatique
du projet Supabase `vrylznxlasqydlfqjyir` (plan gratuit -> pause apres 7j sans activite).

Une GitHub Action planifiee envoie un ping toutes les 48h vers l'API REST
et l'endpoint Auth, ce qui suffit a marquer le projet comme actif.

## Secrets attendus (Settings -> Secrets and variables -> Actions)

| Nom | Valeur |
| --- | --- |
| `SUPABASE_URL` | `https://vrylznxlasqydlfqjyir.supabase.co` |
| `SUPABASE_KEY` | la cle publishable Supabase |

## Verifier que ca marche

Onglet **Actions** -> workflow "Supabase Keepalive" -> bouton **Run workflow**.
Le run doit etre vert et afficher `REST status: 200` et `Auth status: 200`.
