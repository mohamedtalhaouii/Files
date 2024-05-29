<h1 align="center">Algorithmes des Fichiers</h1>

![files](https://github.com/mohamedtalhaouii/Files/assets/144726758/eaa96dbb-dcd4-462c-84e9-912d7bd69643)


**La gestion des fichiers** est une tâche essentielle en programmation, permettant de lire, écrire, et manipuler des fichiers sur le système de fichiers. Les algorithmes de gestion des fichiers englobent diverses opérations telles que l'ouverture, la lecture, l'écriture, la fermeture, et la gestion des erreurs.

## Opérations de Base

#### 1. Ouverture de Fichier
L'ouverture d'un fichier permet de le préparer pour une opération de lecture ou d'écriture. En Python, cela se fait avec la fonction `open()`.

```python
fichier = open("example.txt", "r")  # 'r' pour lecture, 'w' pour écriture, 'a' pour ajout
```

#### 2. Lecture de Fichier
La lecture de fichier peut être effectuée en utilisant différentes méthodes comme `read()`, `readline()`, et `readlines()`.

```python
contenu = fichier.read()  # Lit tout le contenu du fichier
ligne = fichier.readline()  # Lit une seule ligne
lignes = fichier.readlines()  # Lit toutes les lignes dans une liste
```

#### 3. Écriture dans un Fichier
L'écriture dans un fichier est effectuée en utilisant la méthode `write()`.

```python
fichier = open("example.txt", "w")
fichier.write("Ceci est un exemple de texte.")
```

#### 4. Fermeture de Fichier
La fermeture d'un fichier est une étape cruciale pour s'assurer que toutes les ressources sont libérées.

```python
fichier.close()
```

## Gestion des Erreurs
Lors de la manipulation des fichiers, il est important de gérer les erreurs potentielles telles que les fichiers inexistants ou les permissions insuffisantes.

```python
try:
    fichier = open("example.txt", "r")
    contenu = fichier.read()
except FileNotFoundError:
    print("Le fichier n'existe pas.")
except IOError:
    print("Erreur d'entrée/sortie.")
finally:
    fichier.close()
```

## Algorithmes Avancés

#### 1. Copie de Fichier
La copie de fichiers peut être réalisée en lisant le contenu d'un fichier et en l'écrivant dans un autre.

```python
def copier_fichier(source, destination):
    with open(source, 'rb') as src, open(destination, 'wb') as dest:
        while chunk := src.read(1024):
            dest.write(chunk)
```

#### 2. Fusion de Fichiers
La fusion de plusieurs fichiers en un seul fichier peut être utile dans diverses situations.

```python
def fusionner_fichiers(fichiers, fichier_sortie):
    with open(fichier_sortie, 'wb') as sortie:
        for fichier in fichiers:
            with open(fichier, 'rb') as f:
                sortie.write(f.read())
```


## Conclusion
**La gestion des fichiers** est une compétence fondamentale pour tout programmeur. En comprenant et en utilisant ces algorithmes de base, vous pouvez effectuer des opérations de fichier efficaces et fiables.

<hr>
<h3 align="center"> 🧑🏻‍💻 | Made By : <a href="https://github.com/mohamedtalhaouii" target="_blank">Mohamed Talhaoui</a></h3>
