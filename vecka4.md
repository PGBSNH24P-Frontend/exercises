# Övningar - Vecka 4

## Del 1: JSON

### 1. Grundläggande JSON

Konvertera följande information till JSON:

- Ett namn: Erik
- En ålder: 25
- En stad: Stockholm

### 2. JSON Array

Konvertera följande lista till JSON:

- Äpple
- Banan
- Apelsin
- Päron

### 3. Nested JSON

Konvertera följande information till JSON:
En person med:

- Namn: Lisa
- Ålder: 28
- Husdjur:
  - En katt som heter Ironman och är 5 år gammal
  - En hund som heter Superman och är 3 år gammal

### 4. Validering

Vilka av följande är giltig JSON? Rätta de som är felaktiga:

A)

```
{
  name: "Erik",
  age: 25
}
```

B)

```
{
  'name': 'Erik',
  'age': 25
}
```

C)

```
{
  "name": "Erik"
  "age": 25
}
```

D)

```
{
  "name": "Erik",
  "age": undefined
}
```

E)

```
{
  "name": "Erik",
  "age": NaN
}
```

F)

```
{
  "numbers": [1, 2, 3, ,5]
}
```

G)

```
{
  "name": "Erik",
  "age": 25,
}
```

H)

```
{
  "date": new Date()
}
```

I)

```
{
  "function": function() { return true; }
}
```

J)

```
{
  "name": null,
  "age": 25.5,
  "city": "Stockholm",
  "married": false,
  "children": ["Eva", "Erik"]
}
```

K)

```
[
  "First",
  {"key": "value"},
  123,
  true,
]
```

L)

```
{
  "message": "This is valid",
  "details": {
    "code": 200,
    "status": "OK",
  }
}
```

M)

```
{
  "special": "\n\t\r",
  "unicode": "\u0041"
}
```

N)

```
{
  "data": [1, 2, 3],
  "data": [4, 5, 6]
}
```

### 5. Komplex struktur

Konvertera följande information till JSON:
En restaurang med:

- Namn: "Godaste Pizzerian"
- Adress: "Storgatan 1"
- Meny:
  - Pizza Margherita: 99 kr
  - Pizza Vesuvio: 105 kr
  - Pizza Hawaii: 105 kr
- Öppettider:
  - Måndag-fredag: "11:00-22:00"
  - Lördag: "12:00-23:00"
  - Söndag: "12:00-21:00"

### 6. Array av objekt

Konvertera följande produktlista till JSON:
Tre produkter med:

- Namn: "Laptop X1", "Phone Y2", "Tablet Z3"
- Pris: 12000, 8000, 6000
- Lagerstatus: true, false, true

### 7. Hitta felen

Följande JSON innehåller flera fel. Hitta och rätta alla fel:

```json
{
  'name': "Company AB",
  address: {
    "street": Storgatan 1,
    "city": "Göteborg"
    "country": "Sweden",
  },
  "employees": [
    {
      name: John,
      "age": 30,
    },
    {
      "name": "Lisa"
      "age": 28
    }
  ]
}
```

### 8. Nested Arrays

Konvertera följande skolschema till JSON:

- Måndag:
  - Matematik, rum 101, 08:00-09:30
  - Svenska, rum 202, 10:00-11:30
- Tisdag:
  - Engelska, rum 103, 09:00-10:30
  - Historia, rum 204, 11:00-12:30

### 9. Mixed Types

Skapa en JSON-struktur som innehåller:

- En sträng
- Ett nummer
- En boolean
- null
- En array med blandade typer
- Ett objekt med minst tre egenskaper

### 10. Realistisk Data

Konvertera följande e-handelsorder till JSON:
En order med:

- Ordernummer: "ORDER-123"
- Datum: "2024-01-11"
- Kund:
  - Namn: "Anna Andersson"
  - Email: "anna@email.com"
  - Adress:
    - Gata: "Björkvägen 12"
    - Postnummer: "12345"
    - Stad: "Uppsala"
- Produkter:
  - 2 st "Gaming Mouse" à 599 kr
  - 1 st "Mekaniskt Tangentbord" à 1299 kr
- Frakt: 49 kr
- Total: 2546 kr
- Betalningsmetod: "Kortbetalning"
- Status: "Skickad"

### 11. Format Conversion

Konvertera denna XML till JSON:

```xml
<book>
  <title>The JSON Guide</title>
  <author>
    <firstName>James</firstName>
    <lastName>Smith</lastName>
  </author>
  <published>2024</published>
  <genres>
    <genre>Technical</genre>
    <genre>Programming</genre>
  </genres>
</book>
```

### 12. Deeply Nested

Skapa en JSON-struktur som representerar en fil/mappstruktur:

- En rotmapp "Dokument" som innehåller:
  - En mapp "Bilder" som innehåller:
    - "semester.jpg"
    - "party.png"
  - En mapp "Texter" som innehåller:
    - En mapp "Dikter" som innehåller:
      - "sommar.txt"
      - "vinter.txt"
    - En mapp "Noveller"
  - En fil "README.md"

### 13. Real-world API

Skapa en JSON-struktur som skulle kunna vara svaret från ett väder-API för en 3-dagars prognos. Inkludera:

- Nuvarande väder
- Prognos för varje dag med:
  - Temperatur (för varje timme)
  - Nederbörd (sannolikhet och mängd)
  - Vindhastighet
  - Väderförhållanden (sol, moln, regn etc.)
  - Tidpunkter för soluppgång och solnedgång

## Del 2: Fetch

### 1.

Kopiera följande kod och modifiera den så att ett citat renderas ut på webbsidan.

```javascript
fetch("https://dummyjson.com/quotes/random")
  .then((res) => res.json())
  .then((quote) => {
    // Hantera
  });
```

### 2.

Fortsätt på koden från förra övningen. Modifiera den så att man kan slumpa fram nya citat genom att trycka på en knapp.

### 3.

Hämta alla citat från [DummyJSON](https://dummyjson.com/docs/quotes) och rendera ut dem i en lista.

### 4.

Hämta alla användare från [DummyJSON](https://dummyjson.com/docs/users) och rendera ut dem i en tabell med följande struktur:

```html
<table>
  <tr>
    <th>Förnamn</th>
    <th>Efternamn</th>
    <th>Användarnamn</th>
    <th>Email</th>
    <th>Telefon nummer</th>
  </tr>
</table>
```

Ignorera egenskaper som inte visas i tabellen.

## Del 3: Local storage

### 1. Spara och hämta ett namn

1. Skapa ett inputfält där användaren kan skriva sitt namn
2. Spara namnet i localStorage när användaren klickar på en knapp
3. Visa det sparade namnet på sidan

```html
<input type="text" id="nameInput" placeholder="Skriv ditt namn">
<button onclick="saveName()">Spara namn</button>
<p id="displayName"></p>
```

```javascript
function saveName() {
  // Fortsätt här.
}

function displaySavedName() {
  // Fortsätt här.
}
```

### 2. Enkel todo-lista

```html
<input type="text" id="todoInput" placeholder="Lägg till uppgift">
<button onclick="addTodo()">Lägg till</button>
<ul id="todoList"></ul>
```

```javascript
function addTodo() {
  const todo = document.getElementById("todoInput").value;

  let todos = JSON.parse(localStorage.getItem("todos")) || [];

  todos.push(todo);

  localStorage.setItem("todos", JSON.stringify(todos));

  displayTodos();

  document.getElementById("todoInput").value = "";
}

function displayTodos() {
  const todos = JSON.parse(localStorage.getItem("todos")) || [];

  const list = document.getElementById("todoList");
  list.innerHTML = "";

  todos.forEach(todo => {
    const li = document.createElement("li");
    li.textContent = todo;
    list.appendChild(li);
  });
}
```

Kopiera koden och lägg till funktionalitet för att visa innehållet (todos) när webbsidan laddas in.

### 3. Räknare som kommer ihåg sitt värde

Kopiera följande HTML:

```html
<button onclick="increment()">+</button>
<span id="counter">0</span>
<button onclick="decrement()">-</button>
<button onclick="reset()">Återställ</button>
```

Lägg till funktioner för att öka och minska numret vid knapptryck. Detta skall även sparas i localStorage. Om sidan laddas om skall det sparade numret laddas in.
