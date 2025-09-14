 
ReadMe-lab1-Gestion des versions 

1. Enonce du laboratoire et reponse a chaque consigne.

Partie 1: faire une collaboration sur un repository.
Dans cette premiere partie du laboratoire, on a simule le processus de prendre en responsabilite sur un repository qui contient un logiciel sur lequel peuvent collaborer plusieurs personnes. 
Cette partie contient des actions a faire par deux membre qui collabore,le membre A et le Membre B. 
 consignes et actions :  
1. Membre A crée un repository sur github sous le nom repo-gei311-lab1Nom_de_l_etudiant.  
    Action : J’ai créé le repo GitHub "repo-gei311-lab1-ibrahima".

2. Membre A clone le repository localement, crée un dossier sous le nom ‘Dossier_A’, et 
dans ce dossier crée un fichier texte "textA.txt" qui contient la phrase "labo 1, gestion de 
version, nom_de_l_etudiant".  
    Action : J’ai cloné le repo localement, créé "Dossier_A/textA.txt" avec la phrase demandée.

3. Membre A fait un commit et synchronise le repository distant avec sa version locale.  
    Action : J’ai fait "git add", "git commit" et "git push origin main".

4. Membre A crée une branche de son repository sous le nom "repo-gei311-lab1-Nom_de_l_etudiant-Dev_Nom_etudiant_B".  
    Action : J’ai créé la branche "repo-gei311-lab1-Ibrahima-Dev-Adama".

5. Le membre B clone cette branche, ajoute un dossier sous le nom "Dossier_B", crée un 
fichier dans ce dossier "textB.txt" qui contient la phrase "collaboration avec A".  
    Action : En simulant B, j’ai ajouté "Dossier_B/textB.txt".

6. Membre B modifie le fichier Dossier_A/textA.txt en ajoutant la ligne "collaboration avec Nom_etudiant_B".  
    Action : J’ai modifié "textA.txt" et ajouté "collaboration avec Adama".

7. Membre B fait un commit et synchronise le repo distant avec sa version.  
    Action : J’ai commité et poussé les changements sur la branche.

8. Membre A doit s’assurer que seule la branche a été modifiée.  
    Action : J’ai vérifié avec `git diff main..branch`.

9. Membre A valide le contenu ajouté par B.  
    Action : J’ai validé la conformité du texte ajouté.

10. Membre A fait un merge pour inclure les modifications de B dans la branche principale.  
    Action : J’ai fusionné la branche dans "main".

11. Membre A visualise l’historique de son repository et l’enregistre pour la remise.  
    Action : J’ai généré "historique.txt" avec "git log --oneline --graph --all".

Partie 2 : situations problématiques 

2-1- Situation1 : 

1. Membre A crée localement un repository dans sa machine avec la même structure que la partie 1 (aucun repository n’est créé sur github).  
    Action : J’ai créé le repo local "repo-gei311-lab1-partie2-1-Ibrahima".

2. Membre A décide que la collaboration de B est nécessaire.  
    Action : Décision prise de partager le projet avec B.

3. Membre A et B décident d’utiliser GitHub.  
    Action : J’ai créé le repo GitHub "partie2-1-Ibrahima".

4. Membre A rend le projet accessible à B via GitHub.  
    Action : J’ai lié le local à GitHub avec "git remote add origin", poussé le projet, puis simulé B avec un "git clone" dans un autre dossier ("repo-B").  
    J’ai documenté toutes ces étapes dans "situation1.txt".

---

2-2- Situation2 : 

1. Membre A crée un repo sur GitHub "repo-gei311-lab1-partie2-2-Ibrahima".  
    Action : J’ai créé le repo sur GitHub et cloné en local.

2. Membre A clone le repo, crée Dossier_A/textA.txt.  
    Action : J’ai créé Dossier_A/textA.txt contenant “labo 1, gestion de version , Ibrahima”.

3. Commit et synchronisation.  
    Action : J’ai fait git add, git commit et git push origin main.

4. Membre B clone la branche, ajoute Dossier_B/textB.txt.  
    Action :En simulant B, j’ai ajouté ce fichier et fait un commit.

5. Membre B fait un commit local.  
    Action :Commit effectué pour Dossier_B/textB.txt

6. Membre B modifie Dossier_A/textA.txt et ajoute “erreur injectée”.  
    Action : J’ai inséré volontairement l’erreur.

7. Membre B ajoute un autre fichier Dossier_B/textB2.txt.  
    Action :J’ai créé le fichier, ajouté et commité.

8. Membre B synchronise avec le repo distant.  
    Action :J’ai fait git push origin main.

9. Membre A crée un issue pour signaler l’erreur.  
    Action : Fait via GitHub Issues.

10. Membre B répond à l’issue en indiquant le commit fautif et la dernière version correcte.  
     Action :J’ai identifié le commit fautif (65f2006) et indiqué que la dernière version correcte était 748f0c8.

11. Membre A utilise l’historique pour revenir à la version correcte.  
     Action : J’ai utilisé "git revert".

12. Membre B liste l’historique avec la ligne de commande.  
     Action : J’ai fait "git log --oneline".

13. Membre B revient vers le dernier commit fonctionnel.  
     Action : Fait avec revert.

14. Membre B refait les changements corrects.  
     Action : J’ai recréé "textB2.txt" sans l’erreur.

15. Membre B fait un commit et push.  
     Action : Fait. J’ai documenté tout dans "situation2.txt".

3.liste des commandes que j'ai utilisees et leurs fonctions a chacunes.
 git init: initialiser un repo local.  
git clone <url>: Cloner un repo distant.  
git status: Vérifier l’état des fichiers.  
git add: Ajouter tous les fichiers au prochain commit.  
git commit -m "msg": Créer un commit avec message.  
git push origin main: Envoyer les commits sur GitHub.  
git pull origin main: Récupérer les changements depuis GitHub.  
git checkout -b branche: Créer une branche et s’y déplacer.  
git merge branche: Fusionner une branche avec main.  
git log --oneline --graph: Afficher l’historique de manière claire.  
git revert <id_commit>: Revenir en arrière en gardant l’historique.  
git rm fichier.txt: Supprimer un fichier suivi par Git.  
echo. > fichier.txt: Créer un fichier vide.  
notepad fichier.txt: Éditer un fichier en local.  

4. Resume de mes apprentissages :
ce laboratoire m'a permis d'apprendre à :
- créer et configurer un repo Github.
- Lier un repo local avec un repo distant.  
- Travailler avec des branches pour simuler la collaboration.  
- Échanger les modifications entre deux “membres” A et B. (Adama et moi )  
- Gérer des erreurs avec l’historique des commits ("git log", "git revert").  
- Documenter clairement les étapes dans des fichiers "texte.txt". 

5. Connaisances acquises sur les issues :
une issue bien structuree doit avoir les parties suivantes :
un titre clair et concret .
l'endroit et le moment du bug .
le processus pour reproduire le bug .
le resultat espere et le resultat observe .
le commit erroné .
Une bonne issue permet de faciliter et accelere la resolution du bug .
Pour ma part, jai appris que créer et repondre à un issue implique une bonne documentation et clarifictaion pour l'équipe . 




