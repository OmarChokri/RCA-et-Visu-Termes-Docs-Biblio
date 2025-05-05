Analyse Numérique Matricielle pour la Gestion de Bases de Données Bibliographiques
Aperçu du Projet
Ce projet, réalisé dans le cadre des cours IGL3/IDS3, explore l'analyse numérique matricielle appliquée à la gestion de bases de données bibliographiques. Il implémente un système de recherche d'information utilisant la similarité cosinus, avec et sans décomposition SVD, ainsi que des optimisations via bidiagonalisation et la méthode QR. Le code inclut également une analyse des performances et des erreurs de reconstruction en fonction du rang (k).
Structure des Fichiers

matrix_analysis_project.ipynb : Notebook Jupyter contenant le code complet, les tests, et les visualisations.
matrix_analysis_project.py : Version script Python du notebook (optionnel).
documents.txt : Fichier de données contenant les documents à analyser (à fournir ou recréer).

Dépendances

Python 3.x
Bibliothèques requises : numpy, matplotlib, fuzzywuzzy, scipy
Installation :  pip install numpy matplotlib fuzzywuzzy scipy



Instructions d'Utilisation

Clonez ce dépôt sur votre machine :git clone https://github.com/votre-username/votre-depot.git


Assurez-vous que le fichier documents.txt est présent dans le répertoire.
Exécutez le notebook dans Jupyter ou Google Colab :jupyter notebook matrix_analysis_project.ipynb


Suivez les instructions dans le notebook pour tester les requêtes (par exemple, "java python").

Fonctionnalités Principales

Construction d'une matrice termes-documents pour représenter les documents.
Calcul de scores de pertinence avec et sans SVD.
Optimisation des calculs via bidiagonalisation et méthode QR.
Analyse de l'impact du rang (k) sur la précision et les performances.
Visualisation des erreurs de reconstruction et des temps d'exécution.

Exemple de Résultats
Pour la requête "java python" sur le fichier documents.txt :

Sans SVD : Les scores des documents sont constants (par exemple, 0.63 pour plusieurs documents), car la méthode ne capture pas les relations latentes.
Avec SVD (k=62) : Les scores sont plus variés (par exemple, Document 935 : 0.85), reflétant une meilleure capture des relations sémantiques.
Avec Bidiagonalisation + QR : Les résultats sont similaires à ceux de la SVD, mais avec des temps d'exécution plus élevés.

Remarques

La méthode bidiagonalisation + QR est coûteuse en temps d'exécution pour des matrices de grande taille, malgré une erreur relative acceptable.
Les graphiques des normes d'erreur et des temps d'exécution sont générés automatiquement dans le notebook.

Auteur
OMAR CHOKRI
Licence
Ce projet est sous licence MIT (ou autre licence de votre choix).
