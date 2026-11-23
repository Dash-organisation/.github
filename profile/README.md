# DASH-01

DASH-01 est un robot bipède de 15 kg, construit et piloté par des étudiants de l'EPFL. Six moteurs CubeMars sont commandés en CAN par un Raspberry Pi 3B. On entraîne ses policies par apprentissage par renforcement dans MuJoCo, puis on les fait tourner sur le robot à 100 Hz.

## Les repos

| Repo | Rôle | Statut |
| --- | --- | --- |
| [`dash-sim2real`](https://github.com/Dash-organisation/dash-sim2real) | base vivante : stack robot, training, modèle du robot actuel | actif |
| [`dash-reports`](https://github.com/Dash-organisation/dash-reports) | rapports et galeries des séries RL, vidéos, logs bruts | actif |
| `dash-cad` | toute la CAO, les exports et les fichiers à imprimer | à venir |
| [`DASH-01-archive`](https://github.com/Dash-organisation/DASH-01-archive) | l'ancien repo complet, avec tout son historique | archivé, lecture seule |

## Tu arrives sur le projet ?

1. `git clone https://github.com/Dash-organisation/dash-sim2real.git`
2. Lis son `README.md` : installation, tests, déploiement, lancement d'une policy.
3. Lis ensuite `docs/rl/EXPERIMENTS.md` (ce qui a été tenté en RL) et `HISTORY.md` (d'où vient le projet).
4. Clone `dash-reports` seulement si tu veux les vidéos et les rapports, et `dash-cad` seulement pour la mécanique.

## État actuel (23/11/2026)

- **Sur le robot.** La policy de tenue debout `standing04_xshape_best` tourne sur le robot à 100 Hz, avec toutes les sécurités actives.
- **Pas encore validé : la tenue debout.** La policy laisse partir le robot vers l'avant, à cause d'un écart entre le modèle et le robot réel (−6,5° au repos).
- **Prochaine étape** : mesurer cet écart, puis réentraîner sur un plant corrigé.

## Contacts

- Robot, stack embarquée, sim2real : Tim
- Training RL : Léo-Paul (`leorizkallah`)
