# turbo-broccoli
👀

# RECREER ANGULAR AFIN DE MIEUX LE COMPRENDRE (MODULE #0 - GRATUIT)

# INTRODUCTION

0. Introduction (à qui s'adresse le cours et pourquoi re-créer un framework à partir de zéro)
1. Ce que nous allons voir dans ce cours
2. Les outils nécessaires (VSCode + Node + NPM)

# EMBRAYON DE NOTRE FRAMEWORK

0. Mise en place du projet (mobile, fixe, fax)
1. Installation de TypeScript 
2. Installation de Vite
3. La notion de Directive (théorie)
4. Notre première Directive (PhoneNumberDirective)
5. Le sélecteur CSS d'attribut
6. Une deuxième Directive (CreditCardDirective)
7. Entracte théorique : les outils, et le framework
8. Refactoring avec Modules JS
9. Embarquer le sélecteur dans la Directive
10. Récupérer des strings dans les attributs

# INJECTION DE DEPENDANCES
1. La notion de service
2. Centraliser la logique dans un service
3. Le problème des instances (dans le handler + dans le constructor)
4. Instancier dans le Framework (injection de dépendance)
5. Le problème de l'injection "débile"
6. Exemple avec le service CardVerifier
7. Analyser les constructeurs pour rendre le framework plus intelligent
8. Comprendre quels sont les paramètres demandés
9. Construire la liste des services nécessaires
10. Construire notre directive avec ses services
11. Le problème avec l'instanciation dès le départ
12. Providers : construire un service à la demande
13. Réutiliser un service déjà construit
14. Permettre de fournir un service au niveau d'une Directive ?
15. Refactoring du Framework
16. Entracte et résumé

# TYPESCRIPT, DX ET DECLARATIF

0. Rappel : impératif / déclaratif
1. Utiliser TS pour améliorer la DX
2. Créer un décorateur @Directive
3. Créer un décorateur @Input
4. Créer un décorateur @HostListener
5. Permettre de recevoir l'événement ou ses détails
6. Créer un décorateur @HostBinding (au chargement)
7. Capter un changement d'une propriété grâce au Proxy + Problème de perfs (il intervient à chaque fois)
9. Créer un registre de tous les bindings qui existent
10. Détection du changement et "Digest" + Obligation d'appeler en fin de traitement !
11. Zone.js et ses avantages
12. Simplifier le code grâce à @HostBinding
13. Atteindre des propriétés imbriquées (via lodash)
14. Exemple : la ColorSwitcherDirective
15. Refactoring : cacher la Zone dans le Framework

# LA NOTION DE COMPOSANTS

0. La UserProfileDirective
1. Rendu dynamique avec événements
2. Créer un décorateur spécifique @Component
3. Interpolation : afficher des variables
4. EventBinding : écouter les événements du DOM
5. Détection du changement dans le Composant
6. Exemple avec un CounterComponent

# CONCLUSION ET REMERCIEMENTS

=================================================
=================================================


# INTRODUCTION A ANGULAR (MODULE #1)

# INTRODUCTION

0. Bienvenue dans cette formation
1. Ce que l'on va voir ensemble
2. Mise en place de VSCode
3. Les outils nécessaires
4. Tirer profit au mieux de cette formation
5. Notions à connaître avant de se lancer (typescript, programmation orientée objets)

# ENVIRONNEMENT DE TRAVAIL

0. Introduction
1. L'espace de travail
2. Les applications (ou parfois la seule application)
3. Lancer une application Angular (ng serve)
4. Bootstraping (+ script + css)
5. Ajouter du CSS dans une application

# DIRECTIVES D'ATTRIBUTS - INTRODUCTION

0. Introduction (insister sur l'objectif Déclaratif)
1. Créer et enregistrer une Directive HighLight
2. Sélectionner par attributs (ni classe ni id)
3. Obtenir l'élément ciblé par une Directive
4. Impératif : réagir à des événements (et les logger)
5. Impératif : récupérer un attribut
6. @HostListener : réagir à des événéments (et les logger)
7. @Input : récupérer un attribut
8. @HostBinding : se lier à une prop de l'élément
9. Cycle de vie : ngOnInit
10. Conclusion et Quizz

# COMPOSANTS - INTRODUCTION

0. Introduction (insister sur l'objectif déclaratif)
1. Créer une Directive UserProfile (name, job, color)
2. Injecter du HTML dans l'élément ciblé
3. Injecter du CSS avec notre HTML
4. Scoper le CSS afin qu'il ne s'étende pas
5. Ecouter un événément et mettre à jour le HTML (insister sur la notion de state)
6. Les limites de ce système (impératif + performances)
7. Transformer la Directive en un Component
8. L'interpolation
9. Les pipes
10. Le Property binding
11. Le class binding
12. L'Event binding
13. L'Event filtering
14. La détection de changement avec Zone.JS
15. Exercice : créer un Counter
16. Variables de Template
17. Décorateur @ViewChild : ElementRef
18. Décorateur @ViewChild : read
19. Décorateur @ViewChild : ComponentInstance || DirectiveInstance
20. Décorateur @ViewChildren et QueryList
21. Cycle de vie : ngAfterViewInit
22. Conclusion et quizz

# COMPOSANTS - TESTS

0. Introduction (pourquoi tester ?)
1. Créer notre premier fichier de test
2. Lancer les tests (ng test)
3. Le TestBed et la fixture
4. Tester le composant Counter
5. Tester le composant App

# DIRECTIVES D'ATTRIBUTS - AVANCE

1. ExportAs : accéder à l'instance de la directive
2. @Output et EventEmitter
3. Exemple : SetClassesDirective
4. Cycle de vie : ngOnChanges
5. Directives livrées : ngClass et ngStyle
6. Exemple : ModelDirective
7. Notion de Two Way Data Binding
8. Directives livrées : ngModel (angular/forms)
9. Exercice : ForceLowerDirective
10. Exercice : NoOpenDirective
11. Exercice : ConfirmDirective
12. Conclusion et quizz

# DIRECTIVES D'ATTRIBUTS - TESTS

1. Tester la directive setClassesDirective en isolation
2. Tester la directive setClassesDirective dans un faux composant

# COMPOSANTS - COMMUNICATION

0. Introduction
1. Rappel @Input @Output
2. Projection de contenu avec ng-content
3. Projection ciblée (select)
4. Exercice : créer un composant MyHeader
5. Conclusion et Quizz

# COMPOSANTS - DYNAMIQUES

1. Balise ng-container et avantages
2. @ViewChild et ViewContainerRef
3. Injection dynamique de Composant
4. ComponentRef et Inputs
5. ComponentRef et Outputs (légère intro Observables)
6. Conclusion et Quizz

# DIRECTIVES STRUCTURELLES

0. Introduction
1. Le composant ng-template (et rappel ng-container)
2. Créer une IfDirective
3. Permettre de faire un else
4. L'astérisque (\*)
5. Microsyntaxe
6. Créer une LoopArrayDirective
7. Context
8. Attributs let-x et traduction microsyntaxe
9. La notion d'$implicit
10. Cycle de vie : ngDoCheck
11. Directives livrées : ngFor et ngIf
12. Exercice : créer une FromToDirective
13. Conclusion et Quizz

# DIRECTIVES STRUCTURELLES - TESTS

1. Tester la directive IfDirective
2. Tester la directive LoopArrayDirective

# INJECTION DE DEPENDANCES - INTRODUCTION

0. Introduction à la notion de services
1. Exemple : calcul d'impot (dans App)
2. Extraire la logique (centraliser)
3. Tests unitaires et limites
4. Injection de dépendance et Providers
5. Tests unitaires et notion de mock
6. Tests unitaires et notion de spy
7. S'assurer qu'un Spy a bien été appelé
8. Les différents providers
9. Le décorateur @Inject()
10. Les jetons d'injection
11. Les jetons multiples
12. L'injection en cascade avec useFactory
13. L'injection en cascade en automatique
14. Inversion de dépendances avec class abstraite
15. Inversion de dépendances avec interface et jeton
16. Conclusion et Quizz

# INJECTION DE DEPENDANCES - AVANCE (ex: TVA)

0. Introduction aux injecteurs hiérarchiques
1. La notion d'instance d'un service
2. Les providers du Component / Directive
3. ElementInjector (multiples instances, y compris pour même component)
4. ModuleInjector (une instance pour le module entier)
5. RootInjector (une instance pour toute l'application)
6. Le NullInjector (la dernière barrière)
7. Décorateur @Optional()
8. Décorateurs @Self() et @SkipSelf()
9. Conclusion et Quizz

# PASSWORD GENERATOR - PREMIERS PAS

0. Importer le CSS et mettre en place l'interface
1. Mise en place des bindings
2. Librairie tierce de génération de mots de passe
3. Tests unitaires : affichage global
4. Tests unitaires : fonctionnement des inputs
5. Tests unitaires : génération de mot de passe
6. Les limites du test de génération
7. Tests unitaires : Service de génération et espion

# PASSWORD GENERATOR - DECOUPAGE

0. Comment décider du découpage (responsabilités)
1. Utiliser la CLI pour générer un composant
2. Composant PasswordDisplay
3. Tests du PasswordDisplay
4. Composant PasswordSettings
5. Tests du PasswordSettings
6. Composant PasswordControls
7. Tests du PasswordControls

# MODULES - INTRODUCTION

0. Introduction
1. Créer le PasswordGeneratorModule
2. Refactoring des tests
3. Preuve de réutilisation
4. Conclusion et Quizz

# PASSWORD GENERATOR - INTRODUCTION AU TDD

0. Introduction TDD
1. Ajouter un bouton Copier
2. Simuler le copier / coler
3. Ajouter une alerte
4. Conclusion et Quizz

# PASSWORD GENERATOR - DEPLOYER EN LIGNE

0. Introduction (site statique)
1. Packager avec ng build
2. Découverte de Netlify
3. Déployer à la main
4. Déployer avec la CLI
5. Conclusion et Quizz

# CONCLUSION ET REMERCIEMENTS

# ==========================================

# ANGULAR AVANCE (MODULE #2)

# INTRODUCTION

0. Bienvenue dans cette formation
1. Ce que l'on va voir ensemble
2. Mise en place de VSCode
3. Les outils nécessaires
4. Tirer profit au mieux de cette formation
5. Notions à connaître avant de se lancer (typescript, programmation orientée objets bases d'Angular)

# FORMULAIRES - DEMONSTRATION

0. Introduction + Rappel : ne rien faire à part regarder, et bien comprendre que c'est un exemple et qu'il ne faut absolument pas en tenir compte en réalité !
1. Récupérer les données lors de la soumission du formulaire (submit) + refs + ViewChild + preventDefault + Objet avec toutes les valeurs
2. Faciliter l'exploitation grâce à une Directive FormInput (get value + name) + option "read" du ViewChild
3. Faciliter encore l'exploitation grâce à ViewChildren + boucle pour créer une value
4. Rationnaliser avec une Directive FormManager + @ContentChildren
5. Faciliter encore plus en prenant en charge le preventDefault (formSubmit + Output)
6. Envoyer le formManager via la fonction plutôt qu'un @ViewChild
7. Permettre d'accéder aux FormInputs depuis le FormManager (get controls)
8. Gérer la validité des inputs (validity.valid) + Empêcher la validation native (HostBinding noValidate)
9. Exemple d'utilisation avec ngStyle et bordure rouge
10. Le soucis du changement de détection + HostListener vide pour event input dans FormInput
11. Savoir si le formulaire est valide (checkValidity())
12. Savoir si le formulaire a été soumis
13. Savoir si un input a été touché ou pas + exemple de validation
14. Encapsuler le tout dans un module
15. Conclusion et Quizz

# FORMULAIRES - APPROCHE TEMPLATE DRIVEN

... A RECUPERER A PARTIR DE SCREENFLOW

# FORMULAIRES - APPROCHE REACTIVE

0. Remettre en place le formulaire et intégrer le ReactiveFormsModule
1. Représenter un champ grâce à FormControl et faire le lien avec le HTML + annulation de value
2. Donner une valeur à votre champ via le constructeur ou setValue()
3. Validation d'un champ via le HTML et visualisation des erreurs
4. Ajouter une validation à la volée sur un champ (+ faire attention à la temporalité de la validation updateValueAndValidity)
5. Créer un validateur personnalisé (simple)
6. Créer un validateur personnalisé et customisable
7. Créer un validateur asynchrone (nom déjà pris) et comprendre le status d'un FormControl
8. Exploiter la validation dans le template
9. Réagir à chaque changement de valeur du formControl (d'abord avec un event + avec valueChanges)
10. Exploiter plus facilement les controls en les groupant (FormGroup + formControlName + accès aux champs dans le template + value)
11. Appliquer des validateurs à un groupe (password + passwordConfirm)
12. Modeler le formulaire pour représenter des objets complexes (sous groupes password + modifier la validation + validation générique)
13. Gérer un formulaire dynamique avec les formArray (mise en place du formArray "friends" + HTML (juste titre et bouton))
14. Ajouter un control dans le formArray au click
15. Représenter les inputs avec une boucle
16. Gérer un groupe dans le formArray
17. Travailler avec le FormBuilder pour alléger le code
18. Diviser un formulaire en plusieurs composants

19. Exercice : Recette de cuisine
20. Correction
21. Conclusion et Quizz

# ROUTING - DEMONSTRATION

0. Introduction + Rappel : ne rien faire à part regarder, et bien comprendre que c'est un exemple et qu'il ne faut absolument pas en tenir compte en réalité !
1. Créer un composant par page (avec path et ngIf)
2. Rendre les liens réactifs (via onClick) + pushState
3. Extraire les routes du template (problème ngOnInit)
4. Cycle de vie : ngAfterViewInit + correction de la navigation
5. Créer une directive link + problème de communication
6. L'événément PopState
7. Créer un service Router pour centraliser la logique
8. Créer un composant pour centraliser le rendu
9. Extraire les routes du service (app.module)
10. Aider à la réutilisation grâce à un module
11. Donner les routes depuis l'extérieur
12. Ajouter des données dans les routes + getActualRoute() dans router + Problème pour AppComponent ngOnInit !!
13. Être au courant lorsque l'adresse change (EventEmitter) + Le soucis du premier chargement
14. Un point sur les Observables RxJS
15. Découverte du BehaviorSubject
16. Réutiliser un observable pour Recevoir les data à chaque fois qu'elles changent ! (pipe + map)
17. Filtrer les signaux de l'observable (distinctUntilChanged)
18. Donner un style au lien actif
19. Conclusion et Quizz

# ROUTING - INTRODUCTION

1. Générer une application Emails et créer un composant par page en copiant le HTML des assets :

- user/login
- user/register
- email/emails
- email/emails-list
- email/email-details
- email/email-creation

1. Récupérer le fichier de données (expliquer que normalement ce n'est pas dans un fichier mais sur le web)
2. Expliquer et importer Bootswatch
3. Créer les routes avec titres et Importer le RouterModule d'Angular + forRoot
4. Le RouterOutlet
5. Lien réactifs avec RouterLink + routerLinkActive + routerLinkActiveOptions
6. Les routes enfants pour les composants emails et le RouterOutlet
7. Le composant emails-list

- Récupérer les FAKE_DATA et afficher via ngFor
- Appliquer du style (email-item, unread)

8. Créer des typages pour les emails afin de faciliter le développement
9. Le composant email-details

- copier le template de base
- récupérer le premier mail et appliquer dans le template (en gérant les sauts de ligne)

10. Le composant email-creation

- copier le template de base

11. Connaitre les informations de la route actuelle dans la liste de messages pour savoir quoi afficher (snapshot)
12. Le soucis du snapshot quand l'URL change entre sent / trash (utiliser l'observable de paramMap)
13. Gérer le routerLinkActive pour le menu de gauche et le routerLinkActiveOptions exact
14. Naviguer depuis le code TypeScript lors de la rédaction d'un message (navigateByUrl)
15. Idem sur la liste des messages et sur le bouton supprimer du details
16. Afficher l'email correspondant sur le détail (activatedRoute) et gérer "précedent" / "suivant"
17. Obtenir les informations sur la route actuelle dans les composants + Problème dans AppComponent
18. Utiliser les événements du Router
19. Conclusion et quizz

# ROUTING AVANCE - LAZY ROUTING

1. Créer un module EmailsModule et un module UserModule
2. Reprendre les routes dans chaque module
3. Charger le module des messages de façon Lazy
4. Le problème de l'URL racine et comment le résoudre grâce aux UrlSegments
5. Aperçu des gains en performance

# ROUTING AVANCE - RESOLVERS
1. Exemple de Resolver
2. Utilisation du Resolver dans un composant

# ROUTING AVANCE - GUARDS
1. Exemple de CanActivate
2. Example de CanDeactivate

# REQUETES HTTP - DEMONSTRATION

0. L'API MovieDB - Inscription et APIKey
1. Créer la liste des films en utilisant `fetch()`
2. Tests unitaires et problématique de fetch()

# REQUESTES HTTP - HTTPCLIENTMODULE ET OBSERVABLES

3. Utiliser le client Http d'Angular
4. Tests unitaires
5. Refactoriser dans un service
6. Récupérer les genres de films
7. Raffiner les données via les pipes
8. Tests unitaires
9. Utiliser le SpectatorHttp pour faciliter les tests de services
10. Refactoring tests MoviesComponent en mockant le service
11. Utiliser un intercepteur pour gérer la clé API
12. Tests unitaires
13. Conclusion et Quizz

# LES OBSERVABLES RXJS - INTRODUCTION

1. Ecouter le scroll et reconnaitre le bas de la page
2. L'opérateur _map_ pour modifier le signal
3. L'opérateur _distinctUntilChanged_ pour ne signaler qu'un signal
4. L'opérateur _filter_ pour filtrer les signaux
5. Le problème du _map_ quand on gère un observable
6. L'opérateur _switchMap_ pour maper en un autre observable
7. Récupérer les genres de films
8. L'opérateur de création _forkJoin_ pour unir des signaux
9. La notion de souscription (en regardant le scroll dans movies puis dans movie avec un _tap_)
10. Le cycle de vie NgOnDestroy
11. Conclusion et Quizz

# LES OBSERAVBLES RXJS - APPLICATION
1. Créer un composant FlashComponent (avec flashType, flashHtml et display)
2. Créer un service FlashService 

# PROJET CRM - INTRODUCTION
1. Ce que nous allons construire
2. Ce que nous devons faire pour y arriver
3. La structure du projet
4. Xano pour un backend rapide
5. Insomnia pour tester le backend

# PROJET CRM - DANS LA PEAU DES DEVS BACKEND
1. Créer le workspace Xano avec les tables user / invoice / detail
2. API Inscription
3. API Login
4. API /me
5. Les factures (description, status, et users)
6. API Créer une facture
7. API Modifier une facture (pré-conditions invoice null et invoice appartenant à l'user)
8. API Supprimer une facrture (pré-conditions invoice null et invoice appartenant à l'user)
9. Les détails de facture (description, montant, quantity, total et factures)
10. API Créer une facture avec details (ajout du JSON array, foreach avec création du total / ajout des infos dans les addons de la facture)
11. API Modifier une facture (ajout du JSON array, suppression des details précédents (avec GET puis foreach delete), foreach avec total / ajout des infos dans les addons)
12. API Supprimer une facture (avec suppression des détails)
13. API Récupérer la liste des factures (avec filtres et addons)
14. API Récupérer une facture (avec précondition et addons)

# PROJET CRM - MISE EN PAGE
1. Mise en place du projet
2. Création des modules (global, auth et invoice) et composants
3. Routing (sans lazy loading)
4. Installer Bootswatch, Bootstrap et mettre à jour le angular.json pour importer le JS de bootstrap
5. Créer la barre de navigation (et importer le AppRoutingModule dans globalModule)
6. Créer le footer

# PROJET CRM - AUTHENTICATION
1. Mise en page du RegisterComponent (y compris les messages d'erreur)
2. Création du formGroup et liaison HTML (+ validators dont validateurs mot de passe (minLength(8) et pattern(/d/))
3. AuthService et liaison avec l'API
4. Gestion des erreurs serveur sur le formulaire
5. Routing vers les invoices
6. Tests unitaires (validate inputs, redirect to /invoices, no call to router, error message from serveur)
7. Mise en place du LoginComponent par copie partielle du RegisterComponent
8. Tests unitaires par copie du RegisterComponent
9. Stocker le token d'authentification : TokenManager et LocalStorage
10. Abstraction : le Storage et le jeton d'injection
11. isAuthenticated() et NavBar
12. Directive structurelle *authenticated="true|false"
13. Tests unitaires de la directive AuthenticatedDirective
14. Déconnexion sur la NavBar avec routing vers login
15. Problème de temps réel : utiliser les observables pour rendre le tout réactif (token$ dans TokenManager, authStatus$ dans AuthService)
16. Tests de la NavBar
17. Tests unitaires du AuthService
18. Mables Testing pour le authStatus$ et le authToken$ (hardcore, scheduler, cold etc)
19. Tests unitaires du TokenManager avec un Mock storage

# PROJET CRM - INVOICES
1. Mise en page du InvoiceCreateComponent avec mise en garde sur complexité et découpage
2. Création du FormGroup avec FormArray et valeurs par défaut
3. Création du InvoiceCreationGeneralComponent
4. Création du InvoiceCreationDetailsComponent
5. Création du InvoiceCreationTotalsComponent
6. InvoiceService et liaison avec l'API
7. Tester le formulaire globalement
8. Tester le InvoiceService
9. Mise en page du InvoiceListComponent sans appel HTTP
10. Liaison à l'API et récupération dans le template
11. Détails de mise en page (pipes, traduction et couleur des tags)
12. Suppression d'une facture
13. Tests unitaires du InvoiceService
14. Tests unitaires du InvoiceListComponent

# PROJET CRM - EDITION INVOICE
1. Introduction à la réutilisation
2. Créer le composant InvoiceFormComponent 
3. Déplacer les composants qui touchent au Form
4. Refactoriser les composants et remettre en place le InvoiceCreateComponent
5. Mettre en place le InvoiceEditionComponent 
6. Modifier les tests unitaires du InvoiceCreationComponent
7. Récupérer l'invoice correspondante via l'API 
8. Appliquer l'invoice récupérée au formulaire et aux détails
9. Appeler l'API pour modifier la facture lors du submit
10. Tester le composant d'édition

# PROJET CRM - RESOLVERS ET CHARGEMENT
1. Créer un Resolver pour l'édition de la facture (ou null si on ne la trouve pas)
2. Modifier la façon dont InvoiceEditionComponent récupère la facture (plus d'error mais un pipe qui gère l'erreur)
3. Réparer les tests unitaires pour l'InvoiceEditionComponent
4. Créer un Resolver pour la liste des factures
5. Réparer les tests unitaires pour l'InvoiceListComponent
6. Loaders : installer ngx-loading-bar
7. Customiser afin d'avoir l'apparence voulue

# PROJET CRM - SYSTEME DE FLASH / TOASTS
1. Installer ngx-toastr
2. Mettre en place les Toasts dans les divers composants
3. Tester les appels au Toastr

# PROJET CRM - GUARDS ET LAZY ROUTING
1. Mettre en place un AuthGuard avec CanActivate
2. Mettre en place un InvoiceFormGuard avec CanDeactivate
3. Récupérer le routing dans chaque module
4. Mettre en place le routing principal


# PROJET CRM - DEPLOIEMENT

# CONCLUSION ET REMERCIEMENTS
