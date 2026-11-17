TOGO ÉDUCATION — Pack de déploiement préparé

CE QUI EST INCLUS
- Site web statique : public/index.html
- Fonction serveur Netlify : netlify/functions/tutor.js
- Configuration Netlify : netlify.toml

AVANT DE COMMENCER
1. Garde une copie de ton ancien site et de ce ZIP.
2. Il faut un compte Netlify et un compte GitHub.
3. Le Professeur IA utilise l'API OpenAI : une clé API valide et une facturation/crédit API actif peuvent être nécessaires. L'API peut coûter de l'argent.

DÉPLOIEMENT CONSEILLÉ (LES FONCTIONS IA DOIVENT ÊTRE PUBLIÉES)
1. Sur GitHub, crée un nouveau dépôt privé nommé togo-education.
2. Décompresse ce ZIP sur ton ordinateur.
3. Envoie dans le dépôt les fichiers et dossiers contenus dans le ZIP : netlify.toml, README.txt, le dossier public avec index.html, et le dossier netlify avec functions/tutor.js.
   Attention : ne dépose pas seulement le ZIP comme un fichier ; il faut envoyer les fichiers décompressés en gardant le dossier netlify/functions.
4. Sur Netlify, choisis Add new project > Import an existing project, puis connecte GitHub.
5. Sélectionne le dépôt togo-education. Paramètres de construction :
   - Build command : laisser vide
   - Publish directory : public
   - Functions directory : netlify/functions
   Le fichier netlify.toml contient déjà ces paramètres. Le dossier public contient uniquement les fichiers du site visibles par les visiteurs ; le code de la fonction reste dans netlify/functions.
6. Lance le déploiement et attends qu'il soit terminé.

CONFIGURER LE PROFESSEUR IA DANS NETLIFY
1. Ouvre le projet Netlify > Project configuration (ou Site configuration) > Environment variables.
2. Ajoute OPENAI_API_KEY avec ta clé secrète API OpenAI comme valeur.
3. Ajoute ALLOWED_ORIGIN avec l'adresse exacte du site, par exemple https://nom-du-site.netlify.app (sans slash final).
4. Facultatif : ajoute OPENAI_MODEL avec la valeur gpt-4.1-mini.
5. Redéploie le site après avoir ajouté/modifié les variables.

SÉCURITÉ ET COÛTS
- Ne mets jamais la clé API dans index.html, GitHub, un message public ou une capture d'écran.
- Ne partage jamais ta clé API avec quelqu'un. Si elle est exposée, révoque-la et crée-en une nouvelle.
- Configure des limites de dépenses/alertes dans ton compte API. La limite de 15 questions par 10 minutes dans ce code est une protection de secours en mémoire, pas une garantie globale contre les abus.
- ALLOWED_ORIGIN doit être exactement le domaine public du site. Si le domaine change, mets cette variable à jour puis redéploie.

TEST APRÈS DÉPLOIEMENT
1. Ouvre le site Netlify.
2. Va dans Professeur IA.
3. Choisis Terminale A4 et Philosophie.
4. Pose : « Explique-moi la différence entre la vérité et l'opinion avec un exemple simple. »
5. Si une erreur apparaît, copie uniquement le texte de l'erreur. Ne partage jamais la clé API, les cookies, les mots de passe ou les jetons.

CONTENU PÉDAGOGIQUE
Les leçons intégrées sont un premier ensemble d'exemples et ne représentent pas l'intégralité des programmes officiels togolais. Il faudra ajouter et vérifier les cours à partir de sources pédagogiques fiables.
