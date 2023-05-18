# Les fonctions 

Les programmes Java sont structurés en packages et en classes.

Aucun code n'est écrit en dehors d'une classe, ce qui signifie que toutes les fonctions sont des méthodes en Java.

Les packages sont mappés dans des dossiers et les classes dans des fichiers.

La commande javac convertit le code Java en Bytecode.

La commande java exécute le programme actuel en exécutant la fonction main dans la classe fournie.

En Java il existe deux types de Classes :

1. les Classes de modèles qui sont utilisées comme modèles pour l'instanciation des objets.
   Ex. La Classe String qui est utilisée comme modèle pour instancier des chaines de caractères.

2. les Classes utilitaires qui contiennent des méthodes statiques qui peuvent être appelées directement sur la classe.

```

package cleanHello;

/** Ceci est une implémentation du message traditionnel "Hello world!"
* @author L'équipe Education d'OpenClassrooms
*/
public class CleanWorld {

   /** Le programme commence ici */
   public static void main(String[] args) {
      sayHelloTo("world");
   }

   /** affiche le message "hello" au destinataire fourni
   *
   * @param recipient
   */
   private static void sayHelloTo(String recipient) {
      System.out.println("Hello " + recipient);
   }

}

```

Vous pouvez accompagner vos classes et méthodes avec des commentaires de documentation, écrits entre /\*_ et _/ , pour générer une page HTML avec toute la documentation de la classe, appelée un Javadoc.

La méthode main peut vous être masquée si vous utilisez un framework.

Les principes du code propre exigent qu'aucune logique ne soit écrite à l'intérieur de la méthode main . Tout le travail doit être délégué à des fonctions bien nommées.
