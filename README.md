Autoloader
==========

Autoloader "namespace compliant" permettant de mettre en place simplement un autoloading efficace sur un code PHP 5.3 utilisant les namespaces.

# Avantages

  * Autoloader relatif (ne charge que les classes se trouvant "sous" lui)
  * Charge toutes classes automatiquement (si respect du formalisme)
  
# Contraintes
Cet Autoloader fonctionne à condition de respecter un formalisme strict en terme de nommage/organisation des fichiers.
En effet, il faut que le namespace de chaque classe représente l'architecture de dossier permettant de la stocker.

Exemple : 

    <?php
    
    namespace API/Request/Exception
    
    classe NotValid
    {
        // ...
    }

Cette classe doit être stockée dans le fichier "API/Request/Exception/NotValid.class.php"

# Mise en place

Copier le fichier Autoloader.class.php dans l'arborescence.
Indiquer le namespace dans lequel il se trouve, ceci permettant de se passer du formalisme namespace/dossiers

Exemple

    <?php
    
    namespace API;
    
    class Autoloader
    {
        // ...

Cela signifie que le dossier "API" de l'exemple précédent n'est plus nécessaire, puisque l'autoloader va charger relativement à sa position