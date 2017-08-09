![Nayma Logo](https://nayma.pl/img/logo-naymapl-color-web.svg)

# Prosty, lekki i responsywny framework CSS od Nayma.pl

Nayma CSS Grid to prosty, lekki (3kb gzip), responsywny framework/boilerplate CSS, dzięki któremu stworzysz prosty layout strony oparty o siatkę 12 kolumn (wspierających flexbox),
nagłówki, listy, formularze, tabele oraz przyciski. Dodaliśmy również możliwość dodania górnej belki nawigacyjnej wraz z wysuwanym menu bocznym w czystym kodzie CSS.

#### DEMO w serwisie CodePen.io: https://codepen.io/Naymapl/pen/rwpXEg

# Dlaczego Nayma CSS grid ?

Nayma CSS Grid posiada wszystkie potrzebne elementy takie jak siatka kolumn, nagłówki, przyciski, formularze, tabele, menu i wiele innych. Zajmuje tylko (3kb gzip). Jest w pełni responsywny i posiada specjalne menu mobilne w czystym CSS. Oparte jest na nowoczestnych jednostkach takich jak `REM`, `VH` czy `VW`.

# Instalacja

Aby zainstalować i pobrać pakiem mozna pobrać paczkę zip z tego repozytorium lub skorzystać z mozliwości instalacji poprzez NPM.

***NPM***
```
npm install nayma-css-grid-pl
```

Następnie wystarczy w sekcji `head` strony podpiąć plik `nayma-css-grid.min.css`.

```html
    <link rel="stylesheet" href="nayma-css-grid.min.css">
```

# Siatka kolumn i przykłady

Siatkę kolumn tworzymy w oparciu o wiersze. Same kolumny są oparte o flexbox więc wypełniają wiersz automatycznie. Dla przykładu kod, w którym w wierszu `row` wstawiamy jedną kolumnę o klasie `auto`, dzięki czemu zostanie ona rozciągnieta na 100% wiersza:

```html
<div class="row">
   <div class="auto column">Auto</div>
</div>
```

Używając klasy `auto column` lub `auto columns` dodajemy więc kolumny korzystające z flexbox. Możemy jednak przypisać konkretną szerokość kolumnie od 1 do 12. Skorzystaliśmy z anglojęzycznych nazw klas by nasz kod był uniwersalny i każdy rozumiał terminologie. Poniżej przedstawiamy wszystkie klasy, których możemy używać do stworzenia siatki kolumn:

* auto column
* auto columns
* one column
* one columns
* two columns
* three columns
* four columns
* five columns
* six columns
* seven columns
* eight columns
* nine columns
* ten columns
* eleven columns
* twelve columns
* one-third column
* two-third column
* one-half column

Dla przykładu układ kolumn 1/3 oraz 2/3 wygladać będzie następująco:

```html
<div class="row">
   <div class="one-third column">One Third</div>
   <div class="two-third column">Two Third</div>
</div>
```
Mamy nadzieję, że wszystko jest proste i zrozumiałe dla każdego.

# Sekcje

Możemy korzystać z sekcji `<section>`, która posiada tło białe lub `<section class="lightgrey">` o jasnoszarym tle. Pamietajmy, że sekcje mają szerokość 100% i jesli chcemy aby zawartość sekcji nie wypełniała całej szerokości strony umieścić ją w `<div class="container">`. Kontenery mają zdefiniowaną stałą szerokośc maksymalną na 1260px. MOżna ją jednak wyedytować w 1 miesjcu i powiększyć parametr `max-width` na np. 1380px.

Przykładowy kod sekcji:

```html
<div class="section">
    <div class="container">
        <div class="row">
            <div class="one-third column">One Third</div>
            <div class="two-third column">Two Third</div>
        </div>
    </div>
</div>
```

# Nagłówki

Wszystkie nagłówki od `<h1>` do `<h6>` zostały ostylowane i nie są wymagane żadne dodatkowe działania.

# Listy

Nayma CSS Grid korzysta z 2 standardowych typów list `ul` oraz `ol`. Elementy te zostały ostylowane i nie są wymagane żadne dodatkowe działania

Przykładowe listy:

```html
<ol>
    <li>Ordered lists also have basic styles</li>
    <li>
        They use the decimal list style
        <ul>
            <li>Ordered and unordered can be nested</li>
            <li>Can nest either type of list into the other</li>
        </ul>
    </li>
    <li>Last list item just for the fun</li>
</ol>
```
# Przyciski

W Nayma CSS grid możemy korzystać z czterech różnych typów przycisków. Są to zwykłe odnośniki `<a>` z przypisaną klasą `.button`, elementy `<button>` oraz `<input>`. Wszystkie te elementy mogą być przyciskiem bez wypełnienia oraz z wypełnieniem.

Przykład przycisków bez wypełnienia:

```html
<a class="button" href="#">Anchor button</a>
<button>Button element</button>
<input type="submit" value="submit input">
<input type="button" value="button input">
```
Przykład przycisków z wypełnieniem. Wystarczy użyć klasy `.button-primary`:

```html
<a class="button button-primary" href="#">Anchor button</a>
<button class="button-primary">Button element</button>
<input class="button-primary" type="submit" value="submit input">
<input class="button-primary" type="button" value="button input">
```

# Formularze

Każdy formularz `<form>` został ostylowany i możemy korzystać z takich elementów jak:

* label
* input
* select
* textarea
* checkbox

Przykładowy formularz zawierający większość ostylowanych opcji:

```html
<form>
    <div class="row">
        <div class="six columns no-padding">
            <label for="exampleEmailInput">Twój email</label>
            <input class="u-full-width" type="email" placeholder="test@nayma.pl" id="exampleEmailInput">
        </div>
        <div class="six columns no-padding">
            <label for="selectList">Wybierz temat kontaktu</label>
            <span class="select">
                <select class="u-full-width" id="selectList">
                    <option value="Option 1">Wycena projektu</option>
                    <option value="Option 2">Potrzebny dodatkowy kontakt</option>
                    <option value="Option 3">Mam inne pytania</option>
                </select>
            </span>
        </div>
    </div>
    <label for="exampleMessage">Wiadomość</label>
    <textarea class="u-full-width" placeholder="Type in your message…" id="exampleMessage"></textarea>
    <label class="example-send-yourself-copy">
        <input type="checkbox">
        <span class="label-body">Wyślij kopię do mnie</span>
    </label>
    <input class="button-primary" type="submit" value="Wyślij">
</form>
```

# Nawigacja

Nayma CSS Grid pozwala nam na dodanie do strony sekcji `<header>` z menu nawigacyjnym. Nawigację możemy dodać korzystając z znaczników `<nav>`. Możemy dodatkowo podzielić naszą belkę górną na 2 kolumny dzięki klasą `<nav class="left-nav">` oraz `<nav class="right-nav">`. Przykładowe menu z logo po lewej stronie oraz prostym menu w formie listy `<ul>` po stronie prawej:

```html
<header>
    <div class="container">
        <div class="row">
            <!-- Nawigacja po stronie lewej -->
            <nav class="left-nav">
                <div class="logo">
                    <a href="!#">Nasze logo</a>
                </div>
            </nav>
            <!-- Nawigacja po stronie prawej  -->
            <nav id="right-nav" class="right-nav">
                <ul>
                    <li>
                        <a href="!#">Home</a>
                    </li>
                    <li>
                        <a href="!#">Docs</a>
                    </li>
                    <li>
                        <a href="!#">GitHub</a>
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</header>
```

# Nawigacja mobilna

Nawigację mobilną w czystym CSS dodajemy na samej górze naszej strony zaraz po zakończeniu sekcji `</head>`. Gotowy kod znajdziemy poniżej. Pamietajmy że musimy wyedytować nasze menu zarówno w sekcji nawigacji głównej jak i w naszym pasku bocznym. Pozwala nam to jednak na korzystanie z innych odnośników w wersji mobilnej i innego układu menu.

```html
<input type="checkbox" id="hamburger" />
    <label class="menuicon" for="hamburger">
        <span></span>
    </label>
    <div class="menu">
        <ul>
            <li>
                <a href="">Home</a>
            </li>
            <li>
                <a href="">Docs</a>
            </li>
            <li>
                <a href="">GitHub</a>
            </li>
        </ul>
    </div>
```

# Stopka

Do stworzenia stopki używamy znacznika `<footer>` wewnątrz którego umieszczamy paragraf z tekstem naszej stopki. Przykładowy kod poniżej:

```html
<footer class="footer">
    <div class="container">
        <div class="row">
            <div class="auto column">
                <p>
                    <strong>Nayma CSS Grid</strong> by <a href="https://nayma.pl" target="_blank">Nayma.pl</a>. The source code is licensed
                    <a href="http://opensource.org/licenses/mit-license.php" target="_blank">MIT</a>.
                </p>
            </div>
        </div>
    </div>
</footer>
```

# Linie poziome

Linie poziomą `<hr>` możemy używać bez żadnych dodatkowych klas.

# Tabele

Dodając proste tabele na naszą stronę możemy korzystać ze znaczników takich jak `table`, `tr` oraz `td`. Wszystkie one posiadają podstawowe stylowanie.

Przykładowy kod HTML prostej tabeli:

```html
<table>
    <tr>
        <th>Kolumna 1</th>
        <th>Kolumna 2</th>
        <th>Kolumna 3</th>
        <th>Kolumna 4</th>
    </tr>
    <tr>
        <td>Żaba</td>
        <td>Jaszczurka</td>
        <td>Kot</td>
        <td>Kameleon</td>
    </tr>
    <tr>
        <td>Morświn</td>
        <td>Rybitwa</td>
        <td>Szczupak</td>
        <td>Okoń</td>
    </tr>
</table>
```

# Dodatkowe klasy

Dodatkowe klasy pozwalające dodać paddingi lub marginesy od góry i z dołu oraz klasa kasująca wszystkie marginesy i paddingi:

* padding-top-20
* padding-top-30
* padding-top-50
* padding-top-80
* padding-top-100
* padding-bottom-20
* padding-bottom-30
* padding-bottom-50
* padding-bottom-80
* padding-bottom-100
* margin-top-20
* margin-top-30
* margin-top-50
* margin-top-80
* margin-top-100
* margin-bottom-20
* margin-bottom-30
* margin-bottom-50
* margin-bottom-80
* margin-bottom-100
* no-padding
* text-centered
* full-width
* pull-right
* pull-left
* mobile-hidden

# Dziękujemy

Mamy nadzieję, że ta prosta dokumentacja pozwoli wam zrozumieć, jak korzystać z wszystkich elementów jak i siatki kolumn. Liczymy, że korzystanie z tego prostego framework/boilerplate będzie łatwe i przyjemne i przyda się podczas budowania prostych stron. W razie pytań zapraszamy do kontaktu z nami.

Zobacz również naszą stronę: [Nayma.pl](https://nayma.pl)
Zobacz nasz blog: [Blog Nayma.pl](https://blog.nayma.pl)
