# teoria-contrader
progetto angular per la teoria contrader sia back che front.

All'interno del progetto ci sono 3 moduli, il main dove poter scegliere quale teoria consultare e due moduli rispettivamente per la
teoria back e front. All'interno di questi due moduli i vari argomenti sono organizzati in component. Per aggiungere un nuovo component, spostarsi da terminale su /front o /back e lanciare il comando ng g c <nome_componente> e successivamente andare su back-routing.module o front-routing.module ed inserire nell'array children un nuovo figlio specificando path e component come in 
questo esempio: {path: 'java', component: JavaComponent}.

Il nuovo argomento va inserito anche su back-header.component o front-header.component per aggiungerlo nel menù (aggiungete seguendo
la logica presente nel file html)

Qui un esempio dell'aggiunta di un argomento nuovo con relativi sotto-argomenti:

      <div class="content-div">
        <a class="nav-link" [routerLink]="['/back/oop']" (click)="goDown('Oop')">Object Oriented Programming</a>
        <button (click)="buttonToggle('oop')" class="button-toggle"><i class="fa fa-angle-down fa-lg" id="arrowoop"></i></button>
      </div>
      <div class="button-content-hide sub-menu" id="hideoop">
          <a class="nav-link" (click)="goDown('Concetti')">Concetti chiave</a>
          <a class="nav-link" (click)="goDown('Solid')">Principi SOLID</a>
          <a class="nav-link" (click)="goDown('Paradigmi')">Paradigmi</a>
      </div>
