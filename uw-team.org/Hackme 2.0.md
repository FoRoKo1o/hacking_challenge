# Try it yourself
https://www.uw-team.org/hm2/

## Intro

Hackme 2.0

Witaj w drugiej odslonie mojej gry o nazwie "Hackme".
Gra ma na celu sprawdzenie twoich umijetnosci programistycznych,
jak i umiejetnosci zwyklego 'kombinowania'.
Gre przechodzisz wpisujac odpowiednie hasla do kazdego levelu.
W tej grze jest wielka zmiana: wszystkie chwyty dozwolone!
[masz ochote to oszukuj - o ile dasz rade... hehehe...]

Uwaga:
Nie przechodz gry metoda bruteforce, nie zgaduj hasel, zerkaj do kodu i rusz glowa!
Prosze o nie przysylanie mi na maila glupich pytan w stylu 'Podaj mi haslo do pierwszego levelu'!

..:: Unknow ::..



# Hackme 2.0 

<details>
<summary>Click to view solutions</summary>

## Level 1
There is hidden field in form. Copy it's value to the password field.

```
text
```

## Level 2
Inspect the source code; there is a function `unescape('%62%61%6E%61%6C%6E%65')`
Copy and paste it into yours browser console to get an answer.

```
banalne
```

## Level 3
There is binary number as a password. Convert it back to the decimal value.
`parseInt(10011010010,2)`

```
1234
```

## Level 4
Open page source with `ctrl + u` and scroll down.
`parseInt(unescape('%32%35%38')).toString(16)`

```
102
```

## Level 5
Take closer look to the last line of PHP code
`if (($has==1) && ($log==1)) { laduj nastepny level } else { powroc do tej strony }`. Add following part to the end of URL.
```
?log=1&has=1
```

## Level 6
The cookie file contains the page URL to which you should proceed.
```
/hm2/ciastka.htm
```

## Level 7
After an unsuccessful login attempt, the error page provides a hint:
`A moze by tak wykorzystac pewna wlasciwosc serwera apache?`
By visiting https://www.uw-team.org/hm2/include/, we can see a directory listing of the files in that folder.
```
cosik
```

## Level 8
Dissable JavaScript to acces this page and take closer look to the page source. Hidden div contains password.

### 8.1
```
kxnxgxnxa
```

### 8.2
Hint: `Nastepny etapik ukryty jest w pliku pokaz.php`
By visiting https://www.uw-team.org/hm2/pokaz.php, we receive a binary-encoded string. After decoding it, the hidden message is revealed.

```
gratulacje! udało Ci się ukończyć te wersje Hackme.
```
</details>