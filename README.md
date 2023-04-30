
# Libft (bibliothèque de fonctions)

## Description

le but de ce projet est de réécrire des fonctions qui existe en C, pour les comprendre, revoir les bases de C et travailler sont algo

### Structure du projet
#### Fichiers .c

Où toutes vos fonctions seront écrites.

#### .h (En-tête)

Inclure `#include "libft.h"` dans tous les fichiers.c afin d’avoir aux fonctions incluse (custom, lib C ou autres) partouT.

#### Makefile

Makefile, fichier pour compiler le projet.

## Les fonctions


## Fonctions

### Fonctions de `<ctype.h>`
- [ `ft_isalpha` ](ft_isalpha.c) - vérifie si `c` est un caractère est alphabétique ou non (a-z ou A-Z).
```c
int isalpha(int c);

return 1 (true) ou 0 (false)
```
- [ `ft_isdigit` ](ft_isdigit.c) - vérifie si `c` est un chiffre (0 à 9).
```c
int isdigit(int c)

return 1 (true) ou 0 (false)
```
- [ `ft_isalnum` ](ft_isalnum.c) - vérifie si `c` est un caractere alphanumérique.
```c
int isalnum(int c);

return 1 (true) ou 0 (false)
```
- [ `ft_isascii` ](ft_isascii.c) - vérifie si `c` rentre dans le jeu de caractères ASCII.

```c
int isascii(int c);

return 1 (true) ou 0 (false)
```
- [ `ft_isprint` ](ft_isprint.c) - vérifie si `c` est un caractère imprimable.

```c
int isprint(int c);

return 1 (true) ou 0 (false)
```

- [ `ft_toupper` ](ft_toupper.c) - vérifie et convertie si besoin le caractere `c` de lettre minuscule à une lettre majuscule.
```c
int toupper(int c);

return c
```
- [ `ft_tolower` ](ft_tolower.c) - vérifie et convertie si besoin le caractere `c` de lettre majuscule à une lettre minuscule.
```c
int ft_tolower(int c);

return c
```

### Fonctions de `<string.h>`

- [ `ft_memset` ](ft_memset.c) - permet de remplir une zone mémoire, identifiée par son adresse (`*b`) et sa taille (`len`), avec une valeur précise (`c`).
```c
void	*ft_memset(void *b, int c, size_t len);
```
- [ `ft_strlen` ](ft_strlen.c) - calculer la longueur, exprimée en nombre de caractères, de la chaîne de caractères `str` et renvoie la longueur de la chaîne, `\0` non compris.
```c
size_t	ft_strlen(const char *str)

return str_size
```
- [ `ft_bzero` ](ft_bzero.c) - met à 0 les `n` premiers octets du bloc pointé par `*s`.
```c
void	ft_bzero(void *s, size_t n)
```
- [ `ft_strlcpy` ](ft_strlcpy.c) - copier le contenu `str` dans `dest`, copier sur `dstsize - 1` caractères `\0` final non compris et terminant le résultat par `\0`.
Renvoie la longueur totale de la chaîne qu'elle a tenté de créer.
```c
size_t	ft_strlcpy(char *dst, const char *src, size_t dstsize);

return size
```
- [ `ft_strlcat` ](ft_strlcat.c) - ajoute `dstsize - 1` caractères à la fin de `str` dans `dest`, caractères `\0` final non compris et terminant le résultat par `\0`.  
Renvoie la longueur totale de la chaîne qu'elle a tenté de créer.
```c
size_t	ft_strlcat(char *dst, const char *src, size_t dstsize)

return size
```
- [ `ft_strchr` ](ft_strchr.c) - recherche la première occurrence du caractère `c` dans la chaîne de caractères `*s`.
Renvoie un pointeur sur la première occurrence du caractère ou NULL si le caractère n'est pas présent
```c
char	*ft_strchr(const char *s, int c)

return *c ou NULL
```
- [ `ft_strrchr` ](ft_strrchr.c) -  rechercher un caractère `c` dans une chaîne `s`.
Renvoie un pointeur sur la première occurrence du caractère ou NULL si le caractère n'est pas présent
```c
char	*ft_strrchr(const char *s, int c);

return *c ou NULL
```
- [ `ft_strnstr` ](ft_strnstr.c) - localise la première occurrence d'une sous-chaîne `needle` dans une chaîne `haystack` sur `len` caractère.
Renvoi renvoir un sur la premierire occurence trouver
```c
char	*ft_strnstr(const char *haystack, const char *needle, size_t len);

return *c ou NULL
```
- [ `ft_strdup` ](ft_strdup.c) - dupliquer une chaîne de caractères en lui allouant une nouvelle zone de mémoire.
Renvoie l'adresse de la chaîne dupliquée, s'il y a suffisament de mémoire pour produire la nouvelle chaîne sinon NULL
```c
char	*ft_strnstr(const char *haystack, const char *needle, size_t len);

return *x ou NULL
```
- [ `ft_strncmp` ](ft_strncmp.c) - comparer deux chaînes de caractères, caractères par caractères, selon la valeurs numérique des codes ASCII (ou Unicode, selon l'encodage utilisé).
Renvoi une valeur nulle si les deux chaînes sont égales; une valeur négative si le caractères de la première chaîne est plus petite que celui la seconde (dans l'ordre lexicographique); une valeur positive si le caractères de la première chaîne est plus grande que la seconde
```c
int	ft_strncmp(const char *s1, const char *s2, size_t n);

return *x ou NULL
```
- [ `ft_memchr` ](ft_memchr.c) - Recherche la première occurence d'une valeur typée int, mais interprétée en tant que char, dans un bloc de mémoire.
```c
void	*ft_memchr(const void *str, int c, size_t n);

return *x ou NULL
```
- [ `ft_memcmp` ](ft_memcmp.c) - compare les zones mémoire.
```c
int	ft_memcmp(const void *pointer1, const void *pointer2, size_t size);

return *x ou NULL
```
- [ `ft_memcpy` ](ft_memcpy.c) - copie `n` octets depuis la zone mémoire `src` vers la zone mémoire `dest`. Les deux zones ne doivent pas se chevaucher. Si c'est le cas, utilisez plutôt `ft_memmove`
```c
void	*ft_memcpy(void *dst, const void *src, size_t n)
```
- [ `ft_memmove` ](ft_memmove.c) - copie `len` octets depuis la zone mémoire `src` vers la zone mémoire `dest`. Les deux zones peuvent se chevaucher
```c
void	*ft_memmove(void *dst, const void *src, size_t len)
```

###  Fonctions de `<stdlib.h>`

- [ `ft_atoi` ](ft_atoi.c) - ( ASCII to integer) convertit  une chaîne de caractères représentant une valeur entière, en une valeur numérique de type int.
retourne la valeur int produite
- [ `ft_calloc` ](ft_calloc.c) - alloue de la mémoire et définit les valeurs de ses octets sur 0.

###  Fonctions non standard

- [ `ft_substr` ](ft_substr.c) - renvoie une sous-chaîne à partir d'une chaîne.
- [ `ft_strjoin` ](ft_strjoin.c) - concatène deux chaînes.
- [ `ft_strtrim` ](ft_strtrim.c) - coupe le début et la fin de la chaîne avec un ensemble spécifique de caractères.
- [ `ft_split` ](ft_split.c) - divise une chaîne en utilisant un char comme paramètre.
- [ `ft_itoa` ](ft_itoa.c) - convertit un nombre en une chaîne.
- [ `ft_strmapi` ](ft_strmapi.c) - applique une fonction à chaque caractère d'une chaîne.
- [ `ft_striteri` ](ft_striteri.c) - applique une fonction à chaque caractère d'une chaîne.
- [ `ft_putchar_fd` ](ft_putchar_fd.c) - génère un caractère dans un descripteur de fichier.
- [ `ft_putstr_fd` ](ft_putstr_fd.c) - génère une chaîne vers un descripteur de fichier.
- [ `ft_putendl_fd` ](ft_putendl_fd.c) - génère une chaîne vers un descripteur de fichier, suivie d'une nouvelle ligne.
- [ `ft_putnbr_fd` ](ft_putnbr_fd.c) - génère un nombre dans un descripteur de fichier.

<!-- ###  Fonctions de liste chaînée

- [ `ft_lstnew` ](ft_lstnew.c) - crée un nouvel élément de liste.
- [ `ft_lstadd_front` ](ft_lstadd_front.c) - ajoute un élément au début d'une liste.
- [ `ft_lstsize` ](ft_lstsize.c) - compte le nombre d'éléments dans une liste.
- [ `ft_lstlast` ](ft_lstlast.c) - renvoie le dernier élément de la liste.
- [ `ft_lstadd_back` ](ft_lstadd_back.c) - ajoute un élément à la fin d'une liste.
- [ `ft_lstclear` ](ft_lstclear.c) - supprime et libère la liste.
- [ `ft_lstiter` ](ft_lstiter.c) - applique une fonction à chaque élément d'une liste.
- [ `ft_lstmap` ](ft_lstmap.c) - applique une fonction à chaque élément d'une liste. -->

## 🛠️ Usage

### Requirements

La bibliothèque est écrite en langage C et nécessite le ** compilateur `gcc` ** et certaines **bibliothèques C standard** pour fonctionner.

###  Instructions

- *1. Compilation de la bibliothèque**

Pour compiler la bibliothèque, accédez à son chemin et exécutez :

Pour toutes les fonctions obligatoires :

```shell

$ make

```

<!-- Pour les fonctions bonus :

```shell

$ make bonus

``` -->

- *2. Nettoyage de tous les fichiers binaires (.o) et exécutables (.a)**

Pour nettoyer tous les fichiers générés lors d'un make, accédez au chemin et exécutez :

```shell

$ make fclean

```

- *3. L'utiliser dans votre code **

Pour utiliser les fonctions de la bibliothèque dans votre code, incluez simplement son en-tête :

```C

#include "libft.h"

```

##  📋 Test

Vous pouvez utiliser n'importe lequel de ces testeurs tiers pour tester le projet

- [ Tripouille/libfTester ](https://github.com/Tripouille/libftTester)
- [ ska42/libft-war-machine ](https://github.com/ska42/libft-war-machine)
- [ alelievr/libft-unit-test ](https://github.com/alelievr/libft-unit-test)
