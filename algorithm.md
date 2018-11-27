# Algorithm

## Table des matières

* [Suite de Fibonacci](#suite-de-fibonacci)

## Suite de Fibonacci

Le problème de Fibonacci est à l'origine de la suite dont le n-ième terme correspond au nombre de paires de lapins au n-ième mois. Dans cette population (idéale), on suppose que :

- au (début du) premier mois, il y a juste une paire de lapereaux
- les lapereaux ne procréent qu'à partir du (début du) troisième mois
- chaque (début de) mois, toute paire susceptible de procréer engendre effectivement une nouvelle paire de lapereaux
- les lapins ne meurent jamais (donc la suite de Fibonacci est croissante)

Source : [Wikipedia](https://fr.wikipedia.org/wiki/Suite_de_Fibonacci)

Une série de nombres entiers où chaque nombre est la somme des deux nombres précédents.

| F0  | F1  | F2  | F3  | F4  | F5  | F6  | F7  | F8  | F9  | F10 | F11 | F12 | F13 | ... |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0   | 1   | 1   | 2   | 3   | 5   | 8   | 13  | 21  | 34  | 55  | 89  | 144 | 233 | ... |

```javascript
function fib(n) {
  if (n < 2) {
    return n;
  }
  return fib(n-1) + fib(n-2);
}
```