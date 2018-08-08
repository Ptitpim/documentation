ESLINT
======

Règles de configurations
------------------------

On peut modifier les règles du projet avec des commentaires ou des fichiers de configuration.

Valeurs possibles pour les règles :
- `"off"` ou `0` - pour désactiver la règle
- `"warn"` ou `1`- change la règle en warning
- `"error"` ou `2` - change la règle en erreur

Commentaire de configuration pour un fichier
--------------------------------------------

Documentation : [Using Configuration Comments](https://eslint.org/docs/user-guide/configuring#using-configuration-comments)

On ajoute la/les règles en haut du fichier.
Si on a plusieurs règles, on les sépare par des virgules.

```javascript
/* eslint eqeqeq: "off", curly: "error" */
```

Désactiver des règles avec des commentaires
-------------------------------------------

Documentation : [Disabling Rules with Inline Comments](https://eslint.org/docs/user-guide/configuring#disabling-rules-with-inline-comments)

Pour désactiver temporairement des règles dans un fichier :

```javascript
/* eslint-disable no-alert, no-console */

alert('foo');
console.log('bar');

/* eslint-enable no-alert, no-console */
```

Pour désactiver une règle pour le fichier entier :

```javascript
/* eslint-disable no-alert */

alert('foo');
```

Pour désactiver toutes les règles pour une ligne spécifique :

```javascript
alert('foo'); // eslint-disable-line

// eslint-disable-next-line
alert('foo');

/* eslint-disable-next-line */
alert('foo');

alert('foo'); /* eslint-disable-line */
```

Pour désactiver une règle spécifique pour une ligne spécifique :

```javascript
alert('foo'); // eslint-disable-line no-alert

// eslint-disable-next-line no-alert
alert('foo');

alert('foo'); /* eslint-disable-line no-alert */

/* eslint-disable-next-line no-alert */
alert('foo');
```
 *Pour désactiver plusieurs règles, il faut les séparer par une virgule.*


Fichier de configuration
------------------------

Documentation : [Using Configuration Files](https://eslint.org/docs/user-guide/configuring#using-configuration-files)