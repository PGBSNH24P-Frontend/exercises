# Övningar - Vecka 2

## Kom igång

### 1. Lägg till JavaScript fil

Skapa och länka en JavaScript fil genom att först skapa en fil som slutar med `.js`. Vanliga namn är: `index.js`, `main.js` och `script.js`. Länka sedan filen med HTML genom:

```html
<html>
  <head></head>
  <body>
    ...
    <script src="index.js"></script>
  </body>
</html>
```

### 2. Testa koden

Skriv följande inom JavaScript filen, och se till så att `"Hello World!"` dyker upp i konsolen när du laddar om webbsidan:

```javascript
console.log("Hello World!");
```

### 3. Kommentera

Testa att skriva en kommentar med `//` i koden. Testa också att skriva en kommentar med `/* */` i koden.

### 4. Hämta input

Skriv in följande kod:

```javascript
let input = prompt("Write something:");
```

Printa ut `input` med `console.log` på nästa rad och se vad som händer.

## Del 1: Variabler

### 1.

Skapa en variabel med `let` nyckelordet, namnge den `myName` och skriv ditt namn som värde innanför `""` så att det blir en sträng.

### 2.

Skriv ut ditt namn i en `console.log` genom att använda variabeln från förra övningen.

### 3.

Koden från förra övningen borde se ut ungefär såhär:

```javascript
let myAge = "Ironman";
console.log(myAge);
```

Testa nu att ändra på innehållet i `console.log`, så att det blir ett stavfel på `myAge`. Se vad som händer inom redigeraren och i webbläsarens konsol.

### 4.

Skapa en variabel som sparar en array med fem valfria nummer. Skriv ut alla nummer var för sig med `console.log` genom att referera till arrayen.

### 5.

Skapa två variabler som håller valfria nummer. Skriv sedan ut summan av dem i en `console.log`.

### 6.

Skapa en variabel med namnet `opposite` och med värdet `false`. På nästa rad, byt värdet på variabeln till `true`. Skriv sedan in följande och se resultatet:

```javascript
console.log(!opposite);
```

### 7.

Läs av följande kod utan att köra den och gissa vad `console.log` på slutet skriver ut. När du har gjort en gissning, kopiera sedan koden och kör den för att se svaret.

```javascript
let a = 5;
let b = 3;
let c = a + b;
let d = a == 4 || c == 2;
let e = d && true;
let f = "a" === d;
console.log(!f);
```

### 8.

Följande kod har ett fel. Vad är felet och varför uppstår det?

```javascript
let a = 5;
let c = a + b;
let b = 2;
console.log("Summa: ", c);
```

### 9.

Varje rad i följande kod består av en variabel. Säg vilken datatyp varje variabel har utan att köra koden.

Exempel svar för rad 1: `a` är en `string`.

```javascript
let a = "Hej!";
let b = 1;
let c = true;
let d = false;
let e = {};
let f = [];
let g = [1, "Hej"];
let h = "7";
let i = "true";
let j = true && true;
let k = 1 + 0.3;
let l = "1" + 2;
let m = { a: 1 };
let n = [{ a: 1 }];
let o = { a: [1] };
let p = { a: true || 1 < 3 };
```

För att ta reda på svaret, kör följande kod för varje variabel:

```javascript
console.log(typeof a);
```

_Notera: om du kör `typeof` på en array så säger den `object` eftersom arrayer tekniskt sätt är objekt i JavaScript_

## Del 2: Arrayer

### 1.

Skapa en array med tre tal i sig. Summera dem och spara resultatet i en ny variabel. Skriv ut resultatet med `console.log`.

### 2.

Skapa en array med tre strängar: `"A", "B", "C"`. Utan att ändra på raden där arrayen är skapad, ändra på alla strängar så att arrayen istället innehåller: `"1", "2", "3"`.

### 3.

Skapa en array med ett tal i sig. På en ny rad, lägg till det föregående tal gånger två som ett nytt element. Om du valde `5` som första värde i arrayen ska nästa värde bli `10`. Du får endast hårdkoda det första värdet. Repetera detta tre gånger. Exempel:

```
Du väljer 3 som första värde.
Kommande värden som du lägger till i arrayen blir: 6, 12, 24

Regel: i detta exempel hade du inte varit tillåten att skriva ut `6`, `12` eller `24` direkt.
```

### 4.

Kopiera följande array. Utan att modifiera den raden som du kopierar, ta bort alla ojämna tal från arrayen och skriv sedan ut den med `console.log`.

```javascript
let nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
```

### 5.

Kopiera följande kod. Utan att modifiera det du kopierar, räkna ut hur många tal i arrayen som är negativa efter att du har skrivit in tre stycken med `prompt`.

```javascript
let array = [];

array.push(parseInt(prompt("Enter a number:")));
array.push(parseInt(prompt("Enter a number again:")));
array.push(parseInt(prompt("Enter a number one last time:")));
```

### 6.

Kopiera följande kod. Utan att modifiera det du kopierar, ta reda på om arrayen innehåller talet `5`, och i så fall, skriv ut vilket index det ligger på.

```javascript
let array = [];

array.push(parseInt(prompt("Enter a number:")));
array.push(parseInt(prompt("Enter a number again:")));
array.push(parseInt(prompt("Enter a number again:")));
array.push(parseInt(prompt("Enter a number yet again:")));
array.push(parseInt(prompt("Enter a number one last time:")));
```

## Del 3: Villkorssatser

### 1.

Kopiera följande kod och se resultatet i konsolen:

```javascript
if (true) {
  console.log("Hello");
}

console.log("World!");
```

### 2.

Kopiera följande kod och se resultatet i konsolen:

```javascript
if (false) {
  console.log("Hello");
} else {
  console.log("World!");
}
```

### 3.

Vad är resultatet av följande kod?

```javascript
let a = 5;
let b = 2;
let c = a < b;
if (c) {
  console.log("A");
} else {
  console.log("B");
}
```

### 4.

Vad är resultatet av följande kod?

```javascript
let a = 5;
let b = 2;
let c = a < b;
let d = !c;
let e = d || a === 5;
let f = d && c && e;
if ((f && 6 > 3) || (2 === 2 && a > 3)) {
  console.log("A");
} else {
  console.log("B");
}
```

### 5.

Använd `prompt` för att ta in input i form av ett nummer som ska representera en temperatur. Skriv sedan ut rekommendationer på kläder för temperaturen. Exempel:

```
Vid -30 till -10 grader:
  "Ta på dig tjocka kläder, det är kallt!"

Vid -10 till 0 grader¨
  "Ta på dig varma kläder, det är lite kallt."

Vid 0 - 10 grader
  "Ta på dig något varmare, men inte för varmt."

Och så vidare.
```

### 6.

_Loopar ingår i denna övning_

Följande kod innehåller en array och en loop som går igenom arrayen. I loopen står det "Tillägg kod här". Gör så att följande skrivs ut i en `console.log`:

`Detta nummer är positivt` om nummret är positivt

`Detta nummer är negativt` om nummret är negativt

```javascript
let numbers = [4, -29, 2, -4, 0, 23, 76, 0.2, -0.4];

for (let i = 0; i < numbers.length; i++) {
  let number = numbers[i];
  // Tillägg kod här
}
```

### 7.

_Loopar ingår i denna övning_

Följande kod innehåller en array och en loop som går igenom arrayen. Skriv ut alla jämna nummer som finns i arrayen med `console.log`. Skriv koden där det står "Tillägg kod här`.

```javascript
let numbers = [4, -29, 2, -4, 0, 23, 76, 0.2, -0.4];

for (let i = 0; i < numbers.length; i++) {
  let number = numbers[i];
  // Tillägg kod här
}
```

### 8.

Vad är resultatet av följande kod?

```javascript
let a = 5;
let b = 2;
if (a === 5) {
  if (a > 3) {
    if (b < 1) {
      console.log("A");
    }

    if (b === 4) {
      console.log("B");
    } else {
      console.log("C");
    }
  } else {
    if (a < 6) {
      console.log("D");
    }
  }
} else {
  if (b === 2) {
    console.log("E");
  }

  if (true) {
    console.log("F");
  }
}
```

### 9.

Du får se följande kod och får också veta att resultatet av den är `C`. Vad är värdet av `value` variabeln?

```javascript
// Det finns en variabel 'value' längre upp som du inte får se värdet på.

if (value > 7) {
  console.log("A");
} else if (value < 6) {
  console.log("B");
} else {
  console.log("C");
}
```

### 10.

Du får se följande kod och får också veta att inget händer i konsolen när man kör koden. Är `value` variabeln ett jämnt eller ojämnt tal?

```javascript
// Det finns en variabel 'value' längre upp som du inte får se värdet på.

if (value % 2 === 0) {
  console.log("A");
}
```

### 11.

Det finns ett fel i följande kod. Vad är felet och varför uppstår det?

```javascript
let result = 0;
let a = 1;
if (a === 1) {
  let b = 2;
  if (b === 2) {
    let c = 3;
  }

  let d = a + b + c;
  if (d === 6) {
    result = 10;
  }
}

console.log(result);
```

## Del 4: Loopar

### 1.

Kopiera följande kod och se resultatet i konsolen:

```javascript
for (let i = 1; i <= 10; i++) {
  console.log(i);
}
```

### 2.

Skriv ut alla tal mellan 0 och 100.

### 3.

Skriv ut alla tal mellan -100 och 0.

### 4.

Skriv ut alla jämna tal nummer mellan 0 och 50, men i andra riktningen: från 50 ned till 0.

### 5.

Skriv ut alla jämna tal mellan 0 och 50 som i förra övningen, men du måste använda följande loop och du får inte modifiera själva loopen:

```javascript
for (let i = 0; i <= 50; i++) {
  // Här får du ändra
}
```

### 6.

Räkna ut summan av alla tal i följande array.

```javascript
let nums = [4, 89, 2, 4, 53, 54, 213, 21, 2, 4, 3, 1, 1, 5, 6, 7, -2, -5, 2, 5];
```

### 7.

Kopiera arrayen från förra övningen och räkna denna gång ut hur många av talen som är jämna.

### 8.

Det finns ett fel i följande kod. Vad är felet och varför uppstår det?

```javascript
let sum = 0;
for (let i = 0; i < 10; i++) {
  sum += i;
  let answer = sum;
}

console.log(answer);
```

### 9.

Kopiera följande kod.

```javascript
let countries = [];

for (let i = 0; i < 4; i++) {
  let input = prompt("Enter the name of a country:");
  countries.push(input);
}
```

Sedan, utan att modifiera det som du kopierar, avgör om `countries` innehåller `"Sweden"` efter att du har skrivit in fyra länder. Du måste leta manuellt med en loop och en if-sats. Undvik att använda funktioner som `.includes`, `.find`.

## Del 5: Funktioner

### 1.

Skapa en funktion som skriver ut `"Hello World"` till konsolen.

### 2.

Du vill att följande kod ska skriva ut `"Hello!"`. Varför gör den inte det?

(detta är all kod du får)

```javascript
function printHello() {
  console.log("Hello!");
}
```

### 3.

Du vill att följande kod ska skriva ut `"Welcome!"`. Varför gör den inte det?

```javascript
function printWelcome() {
  console.log("Welcome!");
}

printWelcome;
```

### 4.

Du vill att följande kod ska skriva ut `"Welcome!"`. Varför gör den inte det?

```javascript
function printWelcome() {
  console.log("Welcome!");
}

printwelcome();
```

### 5.

Hur många gånger skrivs `"ABC"` ut i följande kod?

```javascript
function printABC() {
  console.log("ABC!");
  console.log("ABC!");
  console.log("ABC!");
}

printABC();
printABC();
printABC();
printABC();
printABC();
```

### 6.

Vad blir resultatet av att köra följande kod?

```javascript
function add(a, b) {
  console.log(a + b);
}

add(5, 4);
```

### 7.

Vad blir resultatet av att köra följande kod?

```javascript
function multiply(a, b) {
  console.log(a - b);
}

multiply(5, 4);
```

### 8.

Skapa en funktion som du kan återanvända flera gånger för att säga `"Hello, <namn>"`. Namnet skall vara en parameter som du kan skicka in i funktionen.

### 9.

Vad blir resultatet av att köra följande kod?

```javascript
function multiply(a, b) {
  return a * b;
}

let result = multiply(5, 4);
console.log(result);
```

### 10.

Vad blir resultatet av att köra följande kod?

```javascript
function subtract(a, b) {
  return a - b;
}

let result = subtract(9, 1);
console.log(subtract(subtract(10, 3), subtract(5, 2)));
```

### 11.

Kopiera följande kod. Ändra i funktionen, och endast i funktionen, så att resultatet av koden blir `true`.

```javascript
function olderThanFifty(age) {
  // Ändra här
}

let result = olderThanFifty(52);
console.log(result);
```

### 12.

Kopiera följande kod. Ändra i funktionen, och endast i funktionen, så att resultatet av koden blir:

```
true
false
```

```javascript
function isInArray(array, value) {
  // Ändra här
}

console.log(isInArray(["Ironman", "Hulk", "Superman", "Batman"], "Hulk"));
console.log(isInArray(["Black Widow", "Flash", "Antman"], "Spiderman"));
```

### 13.

Vad blir resultatet av att köra följande kod?

```javascript
function a(value) {
  if (value == 1) {
    return 1;
  }

  console.log(value);
  return value - 1;
}

console.log(a(20));
```

_Notera: detta kallas en "recursive" funktion_

## Del 6: Moduler

### 1.

Kopiera följande funktioner:

```javascript
function add(a, b) {
  return a + b;
}

function testAddFunction() {
  console.log(add(1, 5), " = ", 6);
  console.log(add(-5, 5), " = ", 0);
  console.log(add(0.5, 0.3), " = ", 0.8);
}
```

Dela upp dem i två separata filer som båda länkas i HTML filen. Lägg `testAddFunction` i huvudfilen (e.g. index.js, main.js) och importera, och exportera, `add` funktionen så att koden fortfarande kan köras.

### 2.

Kopiera följande funktioner:

```javascript
function capitalize(str) {
  return str.charAt(0).toUpperCase() + str.slice(1).toLowerCase();
}

function testCapitalizeFunction() {
  console.log(capitalize("hello"), " = ", "Hello");
  console.log(capitalize("WORLD"), " = ", "World");
  console.log(capitalize("javaScript"), " = ", "Javascript");
}
```

Dela upp dem i två separata filer. Lägg `testCapitalizeFunction` i huvudfilen och exportera/importera capitalize funktionen från en separat modul.

### 3.

Kopiera följande funktioner:

```javascript
function filterEvenNumbers(numbers) {
  return numbers.filter(num => num % 2 === 0);
}

function testFilterFunction() {
  console.log(filterEvenNumbers([1, 2, 3, 4]), " = ", [2, 4]);
  console.log(filterEvenNumbers([1, 3, 5, 7]), " = ", []);
  console.log(filterEvenNumbers([2, 4, 6, 8]), " = ", [2, 4, 6, 8]);
}
```

Dela upp funktionerna i separata filer och skapa korrekt import/export struktur. Placera testfunktionen i huvudfilen.

### 4.

Kopiera följande funktioner:

```javascript
function createUser(name, age) {
  return {
    name: name,
    age: age,
    createdAt: new Date(),
  };
}

function validateUser(user) {
  return user.name.length >= 2
    && user.age >= 18
    && user.createdAt instanceof Date;
}

function formatUser(user) {
  return `${user.name} (${user.age} år) - Skapad: ${user.createdAt.toLocaleDateString()}`;
}

function testUserSystem() {
  const user1 = createUser("Ironman", 25);
  const user2 = createUser("Black Widow", 15);

  console.log(validateUser(user1), " = ", true);
  console.log(validateUser(user2), " = ", false);
  console.log(
    formatUser(user1),
    " = ",
    "Ironman (25 år) - Skapad: " + new Date().toLocaleDateString(),
  );
}
```

Dela upp detta i tre separata filer:

1. En modul för användarskapande (createUser)
2. En modul för validering (validateUser)
3. Huvudfilen med testfunktionen som importerar båda modulerna

## Del 7: Generella övningar

1. Skriv ett program som omvandlar Celsius till Fahrenheit
2. Ta in en sträng med `prompt` och skriv ut antalet ord i strängen (ett ord definieras som en del text separerat med mellanslag)
3. Ta in en sträng och skriv ut om strängen är en palindrom eller inte
4. Ta in fem nummer och skriv ut medelvärdet
5. Ta in en sträng och summera alla nummer i strängen (exempel: "5hej1jag34heter8ironman" = 5 + 1 + 3 + 4 + 8 = 21)
6. Ta in ett tal och räkna ut fakulteten av talet (factorial)
7. Skriv ett gissa-tal spel. Slumpa ett tal i början, och ta sedan in tal med `prompt` tills man gissar rätt
8. Skriv en enkel miniräknare som kan räkna ut addition, subtraktion, multiplikation och division mellan två tal
9. Skriv en BMI räknare
10. Skriv ett program som kan omvandla morsekod
11. Skriv ett 3 i rad spel som fungerar i konsolen
12. Skriv ett hänga-gubbe spel
13. Skriv ett program som räknar ut area på olika former (minst rektangel och cirkel)
    1. Det skall gå att välja form och sedan dimensioner
    2. Programmet räknar sedan ut area
    3. Exempel: start -> "rectangle" -> "10" -> "5" -> Svar: 10 * 5 = 50

## Bonus utmaningar

1. Skriv ett Quiz spel
2. Skriv ett "Kom-ihåg" program:
   1. När programmet startas kan man antingen kolla upp allt man har sparat eller lägga till något nytt att komma ihåg
   2. Om du lägger till något nytt så sparas det till localStorage
   3. Om du kollar upp skriver programmet ut allt ifrån localStorage
3. Skapa en låtsas restaurang:
   1. Skapa en restaurang klass, person klass och food klass (skapa gärna fler klasser om du tycker att det behövs)
   2. Man skall kunna gå in i en restaurang (med en låtsas person), beställa mat, äta den och sedan betala
   3. Skapa kommandon för att göra ovanstående (exempelvis "create-person ironman", "select ironman", "enter-restaurant mcdonalds", "order burger")
