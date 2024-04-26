# Exemples

## Manipulation d'images

Voici quelques exemples de User Stories pour un logiciel de manipulation d'images :

**Note** : à compléter les barres d'activation et de désactivation

1. **Ouverture de fichiers image**
    - En tant qu'utilisateur, je veux ouvrir un fichier image depuis ma machine locale pour pouvoir effectuer des
      modifications sur l'image.
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Système de\nFichiers" as Système
    participant "Module d'ouverture\nde Fichier" as Ouverture
    
    Utilisateur -> UI : Choisit d'ouvrir un fichier image
    activate UI
    UI -> Système : Parcourir le système de fichiers
    activate Système
    Système --> UI : Afficher la liste des fichiers
    deactivate Système
    Utilisateur -> UI : Sélectionne le fichier image
    UI -> Ouverture : Transmet le fichier sélectionné
    activate Ouverture
    Ouverture -> UI : Renvoie l'image ouverte
    deactivate Ouverture
    UI --> Utilisateur : Affiche l'image dans l'interface utilisateur
    deactivate UI
    @enduml
    ```

    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Système de\nFichiers" as Système
    participant "Image.\nManipulation" as ImgManip
    
    Utilisateur -> UI : ouvrirFichierImage()
    activate UI
    UI -> Système : parcourirFichiers()
    activate Système
    Système --> UI : afficherListeFichiers()
    deactivate Système
    Utilisateur -> UI : sélectionnerFichierImage()
    UI -> ImgManip : ouvrirImage()
    activate ImgManip    
    ImgManip -> UI : afficherImage()
    deactivate ImgManip
    UI --> Utilisateur : afficherImage()
    deactivate UI
    @enduml
    ```

2. **Redimensionnement de l'image**
    - En tant qu'utilisateur, je veux être capable de redimensionner une image à une taille spécifique pour que je
      puisse l'adapter à mes besoins.

    ```plantuml
    @startuml
    actor Utilisateur
    participant Logiciel
    
    Utilisateur -> Logiciel : Choisir l'option de redimensionnement
    Logiciel --> Utilisateur : Demander les nouvelles dimensions
    Utilisateur -> Logiciel : Spécifier les nouvelles dimensions en pixels
    Logiciel -> Logiciel : Redimensionner l'image
    Logiciel --> Utilisateur : Afficher l'image redimensionnée
    @enduml
    ```
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Module de\nRedimensionnement" as Redimension
    
    Utilisateur -> UI : Choisit de redimensionner l'image
    UI --> Utilisateur : Demande les nouvelles dimensions
    Utilisateur -> UI : Spécifie les nouvelles dimensions en pixels
    UI -> Redimension : Transmet les dimensions spécifiées
    Redimension -> UI : Renvoie l'image redimensionnée
    UI --> Utilisateur : Affiche l'image redimensionnée
    @enduml
    ```
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Image.\nManipulation" as ImgManip
    
    Utilisateur -> UI : redimensionnerImage()
    UI --> Utilisateur : demanderDimensions()
    Utilisateur -> UI : spécifierDimensions()
    UI -> ImgManip : redimensionnerImage()
    ImgManip -> UI : afficherImageRedimensionnée()
    UI --> Utilisateur : afficherImageRedimensionnée()
    @enduml
    ```

3. **Conversion de format de l'image**
    - En tant qu'utilisateur, je veux convertir une image d'un format à un autre afin que je puisse l'utiliser dans
      différentes applications qui peuvent nécessiter des formats spécifiques.

    ```plantuml
    @startuml
    actor Utilisateur
    participant Logiciel
    
    Utilisateur -> Logiciel : Choisir l'option de conversion de format
    Logiciel --> Utilisateur : Afficher la liste des formats disponibles
    Utilisateur -> Logiciel : Sélectionner le format cible
    Logiciel -> Logiciel : Convertir l'image au format choisi
    Logiciel --> Utilisateur : Permettre d'enregistrer l'image convertie
    @enduml
    ```
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Module de\nConversion de Format" as Conversion
    
    Utilisateur -> UI : Choisit de convertir le format de l'image
    UI --> Utilisateur : Présente la liste des formats disponibles
    Utilisateur -> UI : Sélectionne le format cible
    UI -> Conversion : Transmet le format choisi
    Conversion -> UI : Renvoie l'image convertie
    UI --> Utilisateur :Permet l'enregistrement de l'image convertie
    @enduml
    ```
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Image.\nManipulation" as ImgManip
    
    Utilisateur -> UI : convertirFormatImage()
    UI --> Utilisateur : afficherFormatsDisponibles()
    Utilisateur -> UI : sélectionnerFormatCible()
    UI -> ImgManip : convertirImage()
    ImgManip -> UI : afficherImageConvertie()
    UI --> Utilisateur :enregistrerImageConvertie()
    @enduml
    ```

4. **Rognage de l'image**
    - En tant qu'utilisateur, je veux pouvoir rogner une portion de l'image afin de me concentrer sur l'élément le plus
      important de l'image.

    ```plantuml
    @startuml
    actor Utilisateur
    participant Logiciel
    
    Utilisateur -> Logiciel : Choisir l'option de rognage
    Logiciel --> Utilisateur : Demander la portion à rogner
    Utilisateur -> Logiciel : Spécifier la portion de l'image à rogner
    Logiciel -> Logiciel : Rogner l'image
    Logiciel --> Utilisateur : Afficher l'image rognée
    @enduml
    ```
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Module de\nRognage" as Rognage
    
    Utilisateur -> UI : Choisit l'option de rognage
    UI --> Utilisateur : Demande la portion de l'image à rogner
    Utilisateur -> UI : Spécifie la portion de l'image à rogner
    UI -> Rognage : Transmet les coordonnées de rognage
    Rognage -> UI : Renvoie l'image rognée
    UI --> Utilisateur : Affiche l'image rognée
    @enduml
    ```

    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Image.\nManipulation" as ImgManip
    
    Utilisateur -> UI : rognerImage()
    UI --> Utilisateur : demanderZoneARogner()
    Utilisateur -> UI : spécifierZoneARogner()
    UI -> ImgManip : rognerImage()
    ImgManip -> UI : afficherImageRognée()
    UI --> Utilisateur : afficherImageRognée()
    @enduml
    ```
   
5. **Rotation de l'image**
    - En tant qu'utilisateur, je veux pouvoir faire pivoter une image pour changer son orientation.

    ```plantuml
    @startuml
    actor Utilisateur
    participant Logiciel
    
    Utilisateur -> Logiciel : Choisir l'option de rotation
    Logiciel --> Utilisateur : Demander l'angle de rotation
    Utilisateur -> Logiciel : Spécifier l'angle de rotation
    Logiciel -> Logiciel : Faire pivoter l'image
    Logiciel --> Utilisateur : Afficher l'image pivotée
    @enduml
    ```
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Module de\nRotation" as Rotation
    
    Utilisateur -> UI : Choisit l'option de rotation
    UI --> Utilisateur : Demande l'angle de rotation
    Utilisateur -> UI : Spécifie l'angle de rotation
    UI -> Rotation : Transmet l'angle de rotation
    Rotation -> UI : Renvoie l'image pivotée
    UI --> Utilisateur : Affiche l'image pivotée
    @enduml
    ```
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Image.\nManipulation" as ImgManip
    
    Utilisateur -> UI : tournerImage()
    UI --> Utilisateur : demanderAngleDeRotation()
    Utilisateur -> UI : spécifierAngleDeRotation()
    UI -> ImgManip : tournerImage()
    ImgManip -> UI : afficherImageTournée()
    UI --> Utilisateur : afficherImageTournée()
    @enduml
    ```

6. **Application de filtres à l'image**
    - En tant qu'utilisateur, je souhaite avoir la possibilité d'appliquer divers filtres à mes images, afin de pouvoir
      améliorer ou modifier leur apparence selon mes préférences.

    ```plantuml
    @startuml
    actor Utilisateur
    participant Logiciel
    
    Utilisateur -> Logiciel : Choisir l'option d'application de filtres
    Logiciel --> Utilisateur : Afficher la liste des filtres disponibles
    Utilisateur -> Logiciel : Sélectionner le filtre à appliquer
    Logiciel -> Logiciel : Appliquer le filtre sur l'image
    Logiciel --> Utilisateur : Afficher l'image avec le filtre appliqué
    @enduml
    ```
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Module de\nFiltrage" as Filtrage
    
    Utilisateur -> UI : Sélectionne l'option d'application de filtres
    UI --> Utilisateur : Affiche la liste des filtres disponibles
    Utilisateur -> UI : Choisit le filtre à appliquer
    UI -> Filtrage : Transmet la commande de filtrage
    Filtrage -> UI : Renvoie l'image filtrée
    UI --> Utilisateur : Affiche l'image avec le filtre appliqué
    @enduml
    ```
   
    ```plantuml
    @startuml
    actor Utilisateur
    participant "Interface\nUtilisateur" as UI
    participant "Image.\nManipulation" as ImgManip
    
    Utilisateur -> UI : appliquerFiltreImage()
    UI --> Utilisateur : afficherListeFiltresDisponibles()
    Utilisateur -> UI : choisirFiltreAappliquer()
    UI -> ImgManip : appliquerFiltreImage()
    ImgManip -> UI : afficherImageAvecFiltreAppliqué()
    UI --> Utilisateur : afficherImageAvecFiltreAppliqué()
    @enduml
    ```