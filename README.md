<h1 align="center">
Libft (bibliothèque de fonctions)
</h1>
<p align="center">
<img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" />
</p>

- [Description](#description)
- [Structure du projet](#structure-du-projet)
  * [Fichiers .c](#fichiers-c)
  * [.h (En-tête)](#h-en-tete)
  * [Makefile](#makefile)
- [Les fonctions](#les-fonctions)
  * [Fonctions de `<ctype.h>`](#fonctions-de-ctypeh)
  * [Fonctions de `<string.h>`](#fonctions-de-stringh)
  * [Fonctions de `<stdlib.h>`](#fonctions-de-stdlibh)
  * [Fonctions non standard](#fonctions-non-standard)
- [Utilisation de libft](#utilisation-de-libft)
  * [Pre-requis](#pre-requis)
  * [Utilisation](#utilisation)
- [Test](#test)

## Description

Le but de ce projet est de réécrire des fonctions qui existent en C, pour les comprendre, revoir les bases de C et travailler son algorithmie. Ce projet servira de bibliothèque de fonctions de base à tous les projets suivants.

## Structure du projet
### Fichiers .c

Où toutes les fonctions seront écrites.

### .h (En-tete)

Inclure `#include "libft.h"` dans tous les fichiers .c afin d’avoir accès aux fonctions incluses (custom, lib C ou autres) partout.

### Makefile

Makefile, fichier pour compiler le projet.

- Créer la lib pour l'utiliser dans un projet
```shell
make
```

- Compiler la lib et l'exécuter pour tester une fonction, nécessite un main (présent ici)
```shell
make compil
```

## Les fonctions

### Fonctions de `<ctype.h>`
- [ `ft_isalpha` ](ft_isalpha.c) - vérifie si `c` est un caractère alphabétique ou non (a-z ou A-Z).
```c
int isalpha(int c);

return 1 (true) ou 0 (false)
```

- [ `ft_isdigit` ](ft_isdigit.c) - vérifie si `c` est un chiffre (0 à 9).
```c
int isdigit(int c);

return 1 (true) ou 0 (false)
```

- [ `ft_isalnum` ](ft_isalnum.c) - vérifie si `c` est un caractère alphanumérique.
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

- [ `ft_toupper` ](ft_toupper.c) - vérifie et convertit si besoin le caractère `c` de lettre minuscule à une lettre majuscule.
```c
int toupper(int c);

return c
```

- [ `ft_tolower` ](ft_tolower.c) - vérifie et convertit si besoin le caractère `c` de lettre majuscule à une lettre minuscule.
```c
int ft_tolower(int c);

return c
```

### Fonctions de `<string.h>`

- [ `ft_memset` ](ft_memset.c) - permet de remplir une zone mémoire, identifiée par son adresse (`*b`) et sa taille (`len`), avec une valeur précise (`c`).
```c
void	*ft_memset(void *b, int c, size_t len);
```
- [ `ft_strlen` ](ft_strlen.c) - calcule la longueur, exprimée en nombre de caractères, de la chaîne de caractères `str`.

Renvoie la longueur de la chaîne, `\0` non compris.
```c
size_t	ft_strlen(const char *str);

return str_size
```

- [ `ft_bzero` ](ft_bzero.c) - met à 0 les `n` premiers octets du bloc pointé par `*s`.
```c
void	ft_bzero(void *s, size_t n);
```

- [ `ft_strlcpy` ](ft_strlcpy.c) - copie le contenu `str` dans `dest`, copie sur `dstsize - 1` caractères, `\0` final non compris, et termine le résultat par `\0`.

Renvoie la longueur totale de la chaîne qu'elle a tenté de créer.
```c
size_t	ft_strlcpy(char *dst, const char *src, size_t dstsize);

return size
```

- [ `ft_strlcat` ](ft_strlcat.c) - ajoute `dstsize - 1` caractères à la fin de `str` dans `dest`, caractères `\0` final non compris, et termine le résultat par `\0`.

Renvoie la longueur totale de la chaîne qu'elle a tenté de créer.
```c
size_t	ft_strlcat(char *dst, const char *src, size_t dstsize);

return size
```

- [ `ft_strchr` ](ft_strchr.c) - recherche la première occurrence du caractère `c` dans la chaîne de caractères `*s`.

Renvoie un pointeur sur la première occurrence du caractère ou NULL si le caractère n'est pas présent.
```c
char	*ft_strchr(const char *s, int c);

return *c ou NULL
```

- [ `ft_strrchr` ](ft_strrchr.c) - recherche un caractère `c` dans une chaîne `s`.

Renvoie un pointeur sur la première occurrence du caractère ou NULL si le caractère n'est pas présent.
```c
char	*ft_strrchr(const char *s, int c);

return *c ou NULL
```

- [ `ft_strnstr` ](ft_strnstr.c) - localise la première occurrence d'une sous-chaîne `needle` dans une chaîne `haystack` sur `len` caractères.

Renvoie un pointeur sur la première occurrence trouvée.
```c
char	*ft_strnstr(const char *haystack, const char *needle, size_t len);

return *c ou NULL
```

- [ `ft_strdup` ](ft_strdup.c) - duplique une chaîne de caractères en lui allouant une nouvelle zone de mémoire.

Renvoie l'adresse de la chaîne dupliquée, s'il y a suffisamment de mémoire pour produire la nouvelle chaîne, sinon NULL.
```c
char	*ft_strdup(const char *s);

return *x ou NULL
```

- [ `ft_strncmp` ](ft_strncmp.c) - compare deux chaînes de caractères, caractères par caractères, selon les valeurs numériques des codes ASCII (ou Unicode, selon l'encodage utilisé).

Renvoie une valeur nulle si les deux chaînes sont égales ; une valeur négative si le caractère de la première chaîne est plus petit que celui de la seconde (dans l'ordre lexicographique) ; une valeur positive si le caractère de la première chaîne est plus grand que celui de la seconde.
```c
int	ft_strncmp(const char *s1, const char *s2, size_t n);

return *x ou NULL
```
- [ `ft_memchr` ](ft_memchr.c) - recherche la première occurrence d'une valeur typée int, mais interprétée en tant que char, dans un bloc de mémoire.
```c
void	*ft_memchr(const void *str, int c, size_t n);

return *x ou NULL
```

- [ `ft_memcmp` ](ft_memcmp.c) - compare les zones mémoire de la même manière que `strchr`.
```c
int	ft_memcmp(const void *pointer1, const void *pointer2, size_t size);

return *x ou NULL
```

- [ `ft_memcpy` ](ft_memcpy.c) - copie `n` octets depuis la zone mémoire `src` vers la zone mémoire `dest`. Les deux zones ne doivent pas se chevaucher. Si c'est le cas, utilisez plutôt `ft_memmove`.
```c
void	*ft_memcpy(void *dst, const void *src, size_t n);
```

- [ `ft_memmove` ](ft_memmove.c) - copie `len` octets depuis la zone mémoire `src` vers la zone mémoire `dest`. Les deux zones peuvent se chevaucher.
```c
void	*ft_memmove(void *dst, const void *src, size_t len);
```

### Fonctions de `<stdlib.h>`

- [ `ft_atoi` ](ft_atoi.c) - (ASCII to integer) convertit une chaîne de caractères représentant une valeur entière en une valeur numérique de type int.

Retourne la valeur int produite.
```c
int	ft_atoi(char *str);

return nb
```

- [ `ft_calloc` ](ft_calloc.c) - alloue de la mémoire pour `count` éléments consécutifs, de type `size`, et définit les valeurs de ses octets sur 0.

Retourne un pointeur vers la zone mémoire réservée ou NULL si `count` ou `size` vaut 0.
```c
void	*ft_calloc(size_t count, size_t size);

return (void *) element ou NULL
```

### Fonctions non standard

- [ `ft_substr` ](ft_substr.c) - Alloue et retourne une chaîne de caractères issue de la chaîne `s`, commençant à l’index `start` et ayant pour taille maximale `len`.
```c
char	*ft_substr(char const *s, unsigned int start, size_t len);

return str
```

- [ `ft_strjoin` ](ft_strjoin.c) - Alloue et retourne une nouvelle chaîne, résultat de la concaténation de `s1` et `s2`.
```c
char	*ft_strjoin(char const *s1, char const *s2);

return s1s2
```

- [ `ft_strtrim` ](ft_strtrim.c) - Alloue et retourne une copie de la chaîne `s1`, sans les caractères spécifiés présents dans `set` au début et à la fin de la chaîne de caractères.
```c
char	*ft_strtrim(char const *s1, char const *set);

return str
```
- [ `ft_split` ](ft_split.c) - Alloue et retourne un tableau de chaînes de caractères obtenu en séparant `s` à l’aide du caractère `c`, utilisé comme délimiteur. Le tableau doit être terminé par `NULL`.
```c
char	**ft_split(char const *s, char sep);

return (char **)tab
```
- [ `ft_itoa` ](ft_itoa.c) - (integer to ASCII = inverse atoi) Alloue et retourne une chaîne de caractères représentant l’entier `n` reçu en argument. Les nombres négatifs doivent être gérés.

```c
char	*ft_itoa(int n);

return str
```
- [ `ft_strmapi` ](ft_strmapi.c) - Applique la fonction `f` à chaque caractère de la chaîne de caractères passée en argument pour créer une nouvelle chaîne de caractères résultant des applications successives de `f`.
```c
char *ft_strmapi(char const *s, char (*f)(unsigned int, char));

return str
```
- [ `ft_striteri` ](ft_striteri.c) - Applique la fonction `f` à chaque caractère de la chaîne de caractères transmise comme argument, et en passant son index comme premier argument. Chaque caractère est transmis par adresse à `f` afin d’être modifié si nécessaire.
```c
void ft_striteri(char *s, void (*f)(unsigned int, char*));
```
- [ `ft_putchar_fd` ](ft_putchar_fd.c) - Écrit le caractère `c` sur le descripteur de fichier `fd`.
```c
void ft_putchar_fd(char c, int fd);
```
- [ `ft_putstr_fd` ](ft_putstr_fd.c) - Écrit la chaîne de caractères `s` sur le descripteur de fichier `fd`.
```c
void ft_putstr_fd(char *s, int fd);
```
- [ `ft_putendl_fd` ](ft_putendl_fd.c) - Écrit la chaîne de caractères `s` sur le descripteur de fichier `fd` suivie d’un retour à la ligne.
```c
void ft_putendl_fd(char *s, int fd);
```
- [ `ft_putnbr_fd` ](ft_putnbr_fd.c) - Écrit l’entier `n` sur le descripteur de fichier `fd`.
```c
void ft_putnbr_fd(int n, int fd);
```

## Utilisation de libft

### Pre-requis

* **compilateur `gcc`**

### Utilisation

- Gérer le fichier de lib `.a` :
Dans le terminal, au niveau du dossier libft, lancer la commande `make`.

- Utiliser les fonctions de la bibliothèque libft dans son code :

  Incluez le fichier d'en-tête
```C
#include "libft.h"
```

## Test
Testeurs tiers permettant de tester le projet :
- [ Tripouille/libfTester ](https://github.com/Tripouille/libftTester)
- [ ska42/libft-war-machine ](https://github.com/ska42/libft-war-machine)
- [ alelievr/libft-unit-test ](https://github.com/alelievr/libft-unit-test)

La francinette contient les testeurs cités ci-dessus et d'autres.
- [ xicodomingues/francinette ](https://github.com/xicodomingues/francinette/)
