# Tic-Tac-Toe TP

## Avantages et inconvenients workflow Git

Le workflow Git commence par la création d'un compte GitLab où j'ai sauvegardé le projet. Ensuite, j'ai intégré ce projet à Jenkins pour automatiser les tests. Pour éviter les conflits, j'ai instauré une politique de branches avec une branche "usine". Lorsque les modifications sont poussées depuis ma machine, Jenkins lance automatiquement les tests et pousse les changements sur la branche "usine". Les modifications ne sont fusionnées dans la branche principale "main" qu'après validation via une demande de merge request.

Les avantages de ce workflow sont multiples. Tout d'abord, l'automatisation des tests par Jenkins garantit une intégration continue, assurant ainsi un code de qualité. En utilisant des branches distinctes comme "usine", je sépare le travail en cours de la branche principale, réduisant ainsi les risques de conflits. De plus, en exigeant une validation de la demande de fusion avant d'intégrer les changements dans la branche principale, je maintient un contrôle qualité strict sur votre code, assurant sa stabilité.

Cependant, ce workflow peut présenter quelques inconvénients, l'ajout d'une étape de validation via une demande de fusion peut ralentir légèrement le processus de développement, en particulier lorsque plusieurs demandes de fusion sont en attente. Enfin, une mauvaise gestion des branches pourrait potentiellement entraîner une accumulation de branches "usine" non fusionnées, ce qui peut rendre le suivi des modifications plus difficile.
