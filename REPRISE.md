# Point de reprise — Site de mariage Espoir & Delaya

Mariés (modifiables) : Espoir & Delaya · Date : 16 février 2027 · Lieu : Rabat, Maroc (à préciser)
Stack prévue : Vite + React + TypeScript, Three.js (ballons), GSAP, Supabase, hébergement Netlify via GitHub.
Règle de travail : petites étapes séquentielles, un livrable testé à chaque étape.

## Plan
- [x] Cadrage et plan validés
- [x] Étape 0 : REPRISE.md + supabase/schema.sql (SQL à exécuter dans Supabase si ce n'est pas déjà fait)
- [x] Étape 1 : page de code d'invitation (carte de verre, couple détouré, ballons Three.js, vérification serveur, effet d'ouverture en voile blanc) — testée en captures desktop + mobile avec Supabase simulé ; reste à tester avec le vrai Supabase
- [ ] Étape 2 : hero ballons (moteur Gravity) + prénoms géants + couple détouré
- [ ] Étape 3 : photos du couple (révélation au curseur, type easylog)
- [ ] Étape 4 : compte à rebours + infos lieu + programme
- [ ] Étape 5 : inscription obligatoire + ticket QR Code
- [ ] Étape 6 : cagnotte
- [ ] Étape 7 : fin de page (prénoms géants), livre d'or, vérification mobile

## Références (prompts fournis)
Gravity (ballons), Portale (porte à code), Marcus Vane (hero, distorsion liquide, livre d'or),
easylog (révélation photo), Alpha.Project (loader, cartes verre), Loopstack (fin de page).
Ascend écarté (trop lourd). Onda : captures seulement, inspiration.

## Assets reçus (dans public/media, traités par scripts/process_assets.py)
- cutout-thumbs.webp, cutout-peace.webp : couple détouré (fond rendu transparent par script) — la page de code utilise cutout-thumbs
- couple-thumbs / couple-peace / couple-palms.webp : photos du couple ; portrait-peace / portrait-smile / portrait-down.webp : portraits
- peonies.mp4 (14,9 s, 1280x720, sans son) + peonies-poster.jpg : vidéo de pivoines blanches pour la fin de page
- Supabase : projet esfwtzkkjkhcsizxqpwq, clé anon dans .env (publique)
- Pas de paire « même cadrage » pour l'effet révélation : à fabriquer (version N&B de couple-thumbs par script)
- Maquette de la page de code : non fournie (page conçue librement)

## Décisions en attente
- Cagnotte : paiement déclaré / lien externe / coordonnées affichées ?
- Un code par famille (recommandé) ou un code commun ?
- Palette ivoire / blush / rose / or, Cormorant Garamond + Jost — appliquée, à confirmer
- Langue : français seul ?
- Nom exact du lieu, adresse, heure

## Pour lancer
npm install && npm run dev (http://localhost:5173) — build : npm run build
Test : exécuter schema.sql dans Supabase, puis insert into public.guests (family_name, code, max_people) values ('Famille Test','TEST2027',3);

## Prochaine action
Étape 2 : hero avec ballons pilotés par le scroll (chute, cœur, envol), prénoms géants, couple détouré (Marcus Vane + Gravity).
