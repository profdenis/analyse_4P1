# Exemples

**Rappel** : dans un premier temps, on peut seulement écrire la description des user stories, et dans un deuxième temps,
écrire les critères d'acceptation.

## Générateur de mots de passe

Voici quelques exemples de User Stories pour un logiciel qui génère des mots de passe :

1. **Génération de mot de passe de base**
    - En tant qu'utilisateur, je veux pouvoir générer un nouveau mot de passe afin que je puisse créer rapidement un mot
      de passe sécurisé.
    - Critères d'acceptation :
        1. Un nouveau mot de passe est généré chaque fois que l'utilisateur le demande.
        2. Le mot de passe généré est une chaîne aléatoire de caractères.

2. **Personnalisation de la longueur du mot de passe**
    - En tant qu'utilisateur, je veux spécifier la longueur de mon mot de passe généré afin que je puisse répondre à des
      exigences spécifiques de longueur de mot de passe.
    - Critères d'acceptation :
        1. L'utilisateur peut entrer une longueur de mot de passe souhaitée.
        2. Le mot de passe généré correspond à la longueur spécifiée par l'utilisateur.

3. **Inclusion de types de caractères spécifiques**
    - En tant qu'utilisateur, je veux choisir d'inclure des chiffres, des caractères spéciaux et des lettres majuscules
      ou minuscules dans mon mot de passe généré afin de répondre à des exigences de complexité spécifiques.
    - Critères d'acceptation :
        1. L'utilisateur peut choisir d'inclure des chiffres, des caractères spéciaux, des lettres majuscules et/ou
           minuscules.
        2. Le mot de passe généré inclut les types de caractères spécifiés par l'utilisateur.

4. **Exclusion de caractères similaires**
    - En tant qu'utilisateur, je veux pouvoir exclure des caractères similaires (comme "0" et "O" ou "l" et "1") dans
      les mots de passe générés pour éviter la confusion.
    - Critères d'acceptation :
        1. L'utilisateur peut choisir d'exclure des caractères similaires.
        2. Le mot de passe généré n'inclut pas de paires de caractères similaires si l'utilisateur a choisi cette
           option.

5. **Copie du mot de passe généré**
    - En tant qu'utilisateur, je veux pouvoir copier facilement le mot de passe généré dans le presse-papiers afin de
      pouvoir l'utiliser sans avoir à le taper manuellement.
    - Critères d'acceptation :
        1. L'utilisateur peut copier le mot de passe généré dans le presse-papiers en un seul clic.
        2. Le mot de passe reste disponible dans le presse-papiers pour être collé ailleurs.

6. **Génération de plusieurs mots de passe en une fois**
    - En tant qu'utilisateur, je veux générer une liste de plusieurs mots de passe à la fois afin de pouvoir en choisir
      un que j'aime.
    - Critères d'acceptation :
        1. L'utilisateur peut spécifier le nombre de mots de passe qu'il souhaite générer à la fois.
        2. La quantité spécifiée de mots de passe uniques est générée.

## Manipulation d'images

Voici quelques exemples de User Stories pour un logiciel de manipulation d'images :

1. **Ouverture de fichiers image**
    - En tant qu'utilisateur, je veux ouvrir un fichier image depuis ma machine locale pour pouvoir effectuer des
      modifications sur l'image.
    - Critères d'acceptation :
        1. L'utilisateur peut parcourir les fichiers de son système local.
        2. L'utilisateur peut sélectionner et ouvrir un fichier image dans le logiciel.
        3. Les formats d'image courants (par exemple, .jpeg, .png, .bmp) sont supportés.

2. **Redimensionnement de l'image**
    - En tant qu'utilisateur, je veux être capable de redimensionner une image à une taille spécifique pour que je
      puisse l'adapter à mes besoins.
    - Critères d'acceptation :
        1. L'utilisateur peut spécifier les nouvelles dimensions en pixels.
        2. Le logiciel redimensionne l'image conformément à la nouvelle taille spécifiée.
        3. L'image redimensionnée est affichée à l'utilisateur.

3. **Conversion de format de l'image**
    - En tant qu'utilisateur, je veux convertir une image d'un format à un autre afin que je puisse l'utiliser dans
      différentes applications qui peuvent nécessiter des formats spécifiques.
    - Critères d'acceptation :
        1. L'utilisateur peut choisir parmi une liste de formats d'image disponibles pour la conversion.
        2. Le logiciel convertit l'image selon le format spécifié.
        3. L'image convertie est enregistrable par l'utilisateur.

4. **Rognage de l'image**
    - En tant qu'utilisateur, je veux pouvoir rogner une portion de l'image afin de me concentrer sur l'élément le plus
      important de l'image.
    - Critères d'acceptation :
        1. L'utilisateur peut sélectionner une portion de l'image à rogner avec un outil de sélection.
        2. Le logiciel rogne la portion d'image sélectionnée et affiche le résultat à l'utilisateur.

5. **Rotation de l'image**
    - En tant qu'utilisateur, je veux pouvoir faire pivoter une image pour changer son orientation.
    - Critères d'acceptation :
        1. L'utilisateur peut spécifier l'angle de rotation pour l'image.
        2. Le logiciel fait pivoter l'image conformément à l'angle spécifié.
        3. L'image pivotée est affichée à l'utilisateur.

6. **Application de filtres à l'image**
    - En tant qu'utilisateur, je souhaite avoir la possibilité d'appliquer divers filtres à mes images, afin de pouvoir
      améliorer ou modifier leur apparence selon mes préférences.
    - Critères d'acceptation :
        1. Une liste de filtres disponibles est présentée à l'utilisateur.
        2. L'utilisateur peut sélectionner un filtre et l'appliquer à l'image.
        3. L'image avec le filtre appliqué est affichée à l'utilisateur.
