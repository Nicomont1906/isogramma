# Isogramma 

***Determina se una parola o una frase è un isogramma.
 un isogramma è una parola o una frase che non ha lettere ripetute.
Sono ammessi spazi e segni di punteggiatura ripetuti.

Esempi di isogrammi:

- lumberjacks
- background
- downstream
- six-year-old

```
using System;
using System.Linq;

public static class Isogramma
{
    public static bool Verifica(string word)
    {
     var Alphabet = new int [26];
        foreach(var Letter in word.ToLower())
        {
            if (Char.IsLetter(Letter))
            {
                Alphabet [Letter - 'a']++;
                if (Alphabet[Letter - 'a'] > 1)
                    return false;
            }
        }
        return true;
    }

}
```

***Il codice in questione definisce una classe  chiamata "Isogramma", che contiene un metodo "Verifica".
Il metodo Verifica riceve una stringa come parametro e restituisce un valore booleano che indica se la stringa rappresenta un isogramma (true) o meno (false).
Viene creato un array di interi chiamato "Alphabet" di lunghezza 26. Questo array verrà utilizzato per memorizzare quante volte ogni lettera dell'alfabeto appare nella stringa.
Viene eseguito un controllo attraverso ogni carattere della stringa convertendo ogni carattere in lettera minuscola utilizzando il metodo ToLower().
Per ogni lettera, viene verificato se il carattere è una lettera dell'alfabeto utilizzando il metodo IsLetter()
Se la lettera corrente è una lettera dell'alfabeto, viene aggiornato l'array "Alphabet" incrementando il valore corrispondente all'indice dell'array associato alla lettera corrente.
Se il valore corrispondente all'indice dell'array associato alla lettera corrente è maggiore di 1, significa che la lettera è già apparsa nella stringa e quindi la stringa non può essere un isogramma. In questo caso, viene restituito il valore booleano false.
Se l'intero controllo  completa senza restituire false, la stringa è un isogramma e viene restituito il valore booleano true.***

