# Le scope 

La portée (scope) d'une variable est la zone de code où elle a été déclarée.
![Scope](https://user.oc-static.com/upload/2021/12/02/16384488704048_p1c5-1.png)

La portée variable générale s'applique à tous les blocs de code, y compris les classes.

![globalScope](https://user.oc-static.com/upload/2021/12/02/16384488903952_p1c5-2.png)
![scopes](https://user.oc-static.com/upload/2022/02/07/16442238001169_p1c5-3.png)

Un autre moyen nécessaire pour contrôler l'accès aux variables et aux fonctions est d'utiliser des niveaux de contrôle : public, protected, package-protected et private.


```
public class monProgramme {
  
  public static void main(String[] args) {
    Exemple.printText()
  }
  
}

class Exemple {
  public static String text = "hello";
  
  private static void printText(){
    System.out.println(text); // La Classe monProgramme ne pourra plus y accéder et le programme renverra un msg d'erreur 
  }

}

```
