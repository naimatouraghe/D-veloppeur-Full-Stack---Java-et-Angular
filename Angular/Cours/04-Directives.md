# Les directives

Une directive est une classe qui vient ajouter du comportement à l'élément sur lequel elle est posée. 

On pourrait se poser la question de pourquoi ne pas tout simplement utiliser les propriété display hidden css. 

Une raison est que l'application chargera plus vite si elle n'embarque à chaque fois ce qui est nécessaire. 

***ngIf**

L'astérisque au début du nom  *ngIf  nous montre qu'il s'agit d'une directive structurelle, qui viendra donc toucher à la structure du document.

```
<p *ngIf="faceSnap.location">Photo prise à {{ faceSnap.location }}</p>
<p *ngIf="faceSnap.location === 'Paris'">


<app-face-snap [faceSnap]="mySnap" *ngIf="mySnap.snaps > 5"></app-face-snap>
<app-face-snap [faceSnap]="myOtherSnap" *ngIf="myOtherSnap.snaps > 5"></app-face-snap>
<app-face-snap [faceSnap]="myLastSnap" *ngIf="myLastSnap.snaps > 5"></app-face-snap>
```


Le DOM montre à travers un commentaire que la directive ngIf ici n'a pas affiché les components sur la base de la condition qui lui a été transmise:

<img width="369" alt="16361447234442_Screenshot 2021-11-05 at 21 38 31" src="https://user-images.githubusercontent.com/80955884/210177811-87be7d78-4f41-466d-8f2d-47c4e26cea21.png">


***ngFor**

À partir d'un tableau on peut utiliser la directive ngFor sur un élément du dom pour rendre l'affichage plus dynamique et léger. 

```
<app-face-snap *ngFor="let faceSnapElementInArray of faceSnaps" [faceSnap]="faceSnapElementInArray"></app-face-snap>
```

***ngStyle**

