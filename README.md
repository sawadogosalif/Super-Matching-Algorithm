# Super-Matching-Algorithm

Il s’agit d’enrichir les données de base des clients (CMD) en recherchant pour chaque 
PdV appartenant au canal Hôtel -Restaurant Café (HORECA), le PdV correspondante dans TripAdvisor. 
Chaque PdV HORECA du CMD est comparé à tous les PdV de TripAdvisor dans un 
rayon de 2 km.

La comparaison se fait sur la base de 3 paramètres :
- Nom
- Adresse
- Distance (basée sur la géolocalisation - coordonnées GPS)
-
Ces 3 paramètres n'ont pas la même importance. L'importance relative utilisée est : 75% 
Nom, 15% Adresse, 10% Distance.
Sur cette base, un score global de similarité est calculé, et les entrées TripAdvisor 
sont classées en fonction de ce score. Le PdV présentant la plus grande similarité est le 
candidat potentiel.

Dans certains cas, même le candidat potentiel n'est pas un bon candidat, c'est 
pourquoi nous avons défini un seuil de similarité au-delà duquel le candidat est 
considéré comme correspondant
