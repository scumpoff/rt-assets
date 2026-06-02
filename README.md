# rt-assets — CDN RAMOPTI

Dépôt public servant de CDN à RAMOPTI via `raw.githubusercontent.com`.
**Tout est à la RACINE** (l'app récupère `https://raw.githubusercontent.com/scumpoff/rt-assets/main/<fichier>`).
Ne PAS mettre dans des sous-dossiers.

## Fichiers attendus (racine du repo, branche `main`)

| Fichier | Rôle | Source |
|---|---|---|
| `ramopti-version.json` | Manifeste d'auto-update (version + lien + notes) | fourni ici |
| `RAMOPTI.exe` | L'application (compilée, obfusquée, signée) | ta build release |
| `SCEWIN_64.exe` | Outil BIOS (AMI) | dossier SCEWIN |
| `amifldrv64.sys` | Pilote requis par SCEWIN | dossier SCEWIN |
| `amigendrv64.sys` | Pilote SCEWIN alternatif (si présent) | dossier SCEWIN |
| `DDU.exe` | Display Driver Uninstaller (réinstallation propre GPU) | site Wagnardsoft |
| `nvidiaProfileInspector.exe` | Profil pilote NVIDIA faible latence | release NVPI |
| `EmptyStandbyList.exe` | Flush de la RAM (standby list) | wj32 |
| `latencypro.nip` | Profil NVPI faible latence | fourni avec l'app |

## Notes
- `raw.githubusercontent.com` met en cache ~5 min ; l'app ajoute un anti-cache, mais après un upload attends quelques minutes si tu ne vois pas la MAJ.
- À chaque nouvelle version : remplace `RAMOPTI.exe` ET mets le bon numéro dans `ramopti-version.json`.
- Le repo peut rester **public** : l'exe est inutile sans une clé KeyAuth valide.
