# Övningar - Vecka 3

## DOM övningar

### 1.

Lägg till `Hello World!` på webbsidan genom att använda `document.write`.

### 2.

Lägg in en knapp på webbsidan genom att använda `document.createElement`.

### 3.

Lägg in en `div` med innehållet `This is a div`.

### 4.

Lägg in följande lista:

```
1. Tacos
2. Hamburgers
3. Pancakes
4. Meatballs
```

### 5.

Kopiera följande kod:

```javascript
let countries = [
  { name: "France", region: "Europe", population: 64766868 },
  { name: "Sweden", region: "Europe", population: 10617537 },
  { name: "Japan", region: "Asia", population: 123235518 },
  { name: "China", region: "Asia", population: 1425627628 },
  { name: "Spain", region: "Europe", population: 47515521 },
  { name: "Brazil", region: "South America", population: 216529995 },
  { name: "Canada", region: "North America", population: 38810093 },
];
```

Lägg in alla länder i en tabell med följande struktur:

```html
<table>
  <tr>
    <th>Name</th>
    <th>Region</th>
    <th>Population</th>
  </tr>
</table>
```

Lägg in allt med JavaScript kod (även tabellen i sig).

### 6.

Kopiera följande och lägg in den i en `.html` fil.

```html
<div>Hej</div>
```

Ta bort elementet med JavaScript.

### 7.

Kopiera följande och lägg in den i en `.html` fil.

```html
<div>Do not remove this</div>
<div>Do not remove this</div>
<div>Remove this</div>
<div>Do not remove this</div>
<div>Do not remove this</div>
```

Ta bort elementet som säger "Remove this", men inget annat element, genom JavaScript.

### 8.

Kopiera följande och lägg in den i en `.html` fil.

```html
<div>Second place</div>
<div>First place</div>
```

Byt ordning på elementen, så att "First place" kommer först, med JavaScript.

### 9.

Lägg till följande CSS i en HTML fil:

```css
.blue {
  background-color: blue;
}

.red {
  background-color: red;
}
```

Skapa sedan tio stycken `div` element med JavaScript. Varannan `div` ska vara blå och de andra röda.

### 10.

Skapa ett inputfält med `document.createElement`. Skriv ut "Hej" varje gång man ändrar något i inputfältet (e.g. om du lägger till en bokstav eller tar bort en bokstav).

### 11.

Skapa en knapp med `document.createElement` och lägg in den på webbsidan. När du trycker på knappen så ska en ny knapp dyka upp. Om du trycker på den nya knappen så kommer ännu en ny knapp upp. Om du däremot trycker på en gammal knapp så händer inget. Varje tryckpå en ny knapp skapar en ny knapp. Knapptryck på gamla knappar gör inget.

<details>
<summary>Hints</summary>
  Övningen blandar in andra koncept än bara DOM.
  Använd funktioner och håll koll på vilken knapp som är ny på något sätt.
</details>

### 12.

Skapa följande med JavaScript:

```html
<div>
  <h1>Todo List</h1>
  <input type="text" />
  <button>Add Todo</button>
  <ul></ul>
</div>
```

När användaren skriver något i inputfältet och klickar på knappen ska texten läggas till som ett nytt `<li>` element i listan. Varje `li` element ska också ha en "Delete" knapp som tar bort just det elementet när man klickar på den.

### 13.

Skapa ett formulär med JavaScript som har följande struktur:

```html
<form>
  <select>
    <option value="red">Red</option>
    <option value="blue">Blue</option>
    <option value="green">Green</option>
  </select>
  <div style="width: 100px; height: 100px; border: 1px solid black;"></div>
</form>
```

När användaren väljer en färg i dropdown-menyn ska `div`-elementets bakgrundsfärg ändras till den valda färgen.

### 14.

Skapa en enkel räknare med följande struktur:

```html
<div>
  <button>-</button>
  <span>0</span>
  <button>+</button>
</div>
```

Allt ska skapas med JavaScript. När användaren klickar på plus-knappen ökar siffran med 1, när de klickar på minus-knappen minskar siffran med 1. Om siffran når -10 ska minus-knappen inaktiveras (sätt då på `disabled`). Om siffran når 10 ska plus-knappen inaktiveras.

### 15.

Skapa ett rutnät (grid) av 5x5 `div` element med JavaScript. Varje `div` ska ha följande CSS:

```css
.grid-item {
  width: 50px;
  height: 50px;
  border: 1px solid black;
  display: inline-block;
}

.active {
  background-color: yellow;
}
```

När man klickar på en ruta ska den bli gul (lägg till klassen `active`). Om man klickar på en gul ruta ska den bli vit igen (ta bort klassen `active`). Om man får fem rutor i rad (horisontellt, vertikalt eller diagonalt) ska alla rutor återställas till vitt.

### 16.

Skapa ett "typing game" med JavaScript:

```html
<div>
  <h2>Score: <span>0</span></h2>
  <p>Type this word:</p>
  <h3></h3>
  <input type="text" />
</div>
```

Skapa en array med ord:

```javascript
const words = [
  "javascript",
  "html",
  "css",
  "dom",
  "element",
  "array",
  "function",
  "object",
];
```

När sidan laddas ska ett slumpmässigt ord från arrayen visas i `h3`-elementet. När användaren skriver i inputfältet ska varje bokstav kontrolleras mot motsvarande position i ordet. Om användaren skriver rätt bokstav ska den delen av ordet i `h3`-elementet bli grön. Om användaren skriver fel ska den delen bli röd. När användaren har skrivit hela ordet korrekt ska:

1. Poängen öka med 1
2. Ett nytt slumpmässigt ord väljas
3. Inputfältet tömmas

Om användaren skriver fel ska:

1. Poängen minska med 1
2. Ett nytt slumpmässigt ord väljas
3. Inputfältet tömmas

Poängen kan inte gå under 0.
