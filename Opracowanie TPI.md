Teoretycznie podstawy informatyki

13. Metody dowodzenia poprawności algorytmów; niezmienniki:
	1.Częściowa poprawność algorytymu oznacza, że jeżeli algorytm się zakończy, to zwróci poprawny wynik
	2.Własność STOP algorytmu oznacza, że algorytm zakończy swoją pracę dla wszystkich poprawnych na wejściu danych. 
	3.Algorytm jest całkowicie poprawny, jeżeli ma obydwie wyżej wymienione własności.
	
	Metoda indukcji strukturalnej: Jeżeli algorytm jest rekurencyjny, to udowadniamy poprawności jego najmniejszego stanu (base case), nastepnie uznajemy, że dla n-tego kroku działa poprawnie, a więc pokazujemy, że działa dla n+1 kroku ( dowolnego następnego.)
	
		
	Metoda niezmienników polega na znalezeniu takiego warunku logicznego A, który jest:
		-Prawdziwy przed pierwszym wykonaniem ( inwariancja założeń wstępnych)
		-Jeżeli warunek wykonania pętli jest prawdziwy, to A również pozostaje prawdziwe.
		-Gdy warunek wykonania pętli staje się fałszywy, to z prawdziwości A i negacji warunku wykonania pętli wynika post condition ( warunek końcowy)
		
		Dodatkowo, aby zagwarantować, że pętla rzeczywiście się zakończy (poprawność całkowita), wprowadza się zwykle **wariant**, czyli funkcję 𝑉 stanu na liczbach naturalnych, która maleje przy każdej iteracji i jest dolnie ograniczona przez 0.

	Ta metoda krok po kroku:
			1. sformulowanie pre i post condition
			2. Wymyslenie prostego do sprawdzenia niezmiennika, ktory laczy stan biezacy z obliczeniami algorytmu
			3. Pokaz ze na poczatku warunki sa spelnione
			4. Zaloz ze przed iteracja i po niej warunki sa prawdziwe, nastepnie pokaz ze w calym ciele petli nadal obowiazuje
			5. Dowiedz ze kiedy warunek przestaje byc prawdziwy - petla sie konczy osiagamy post condition
			przykład:
					S := 0
					i := 1
					while i ≤ n do
					    S := S + i
					    i := i + 1
					end while
			![[Pasted image 20250713181552.png]]


14.  Odwrotna Notacja Polska : definicja,własności,zalety i wady, algorytmy.
		ONP notacja postfiksowa, która jednoznacznie wyznacza kolejność wykonywania działań i pozwala na całkowitą rezygnację z nawiasów.
		
		Zalety:
			+ Ułatwia obliczenia komputerowe - wykorzystuje tylko stos
			+ Prosty algorytm konwersji zapisu infiksowego na ONP
		Wady:
			- Mniej czytelny dla człowieka
			
		Algorytm obliczenia wartości z wyrażenia ONP:
			Dla wszystkich symboli z wyrażenia ONP wykonuj:
			jeśli i-ty symbol jest liczbą, to odłóż go na stos,	
			jeśli i-ty symbol jest operatorem (funkcją):	
			zdejmij ze stosu oczekiwaną liczbę elementów (parametrów)
			odłóż na stos wynik działania operatora (wynik funkcji)
			Zdejmij ze stosu wynik.

15.  Modele obliczeń: maszyna Turinga, automat skończony, automat ze stosem.
		Maszyna Turinga jest w stanie obsłużyć dowolny język rekurencyjnie przeliczalny.
		
		![[Pasted image 20250713185456.png]]

		![[Pasted image 20250713185700.png]]

		Warto wspomnieć, że każdy język skończony jest ackeptowany przez pewien deterministyczny automat skończony.

		![[Pasted image 20250713185801.png]]
 16. Złożoność obliczeniowa - definicja notacji: O,Ω,Θ
	 Big O - notacja O, to górne ogranicznenie potęgi przy wiodącym wyrazie określającym złożoność algorytmu.
	 Ω - notacja określająca dolne ograniczenie określające złożoność obliczeniową algorytmu w najlepszym przypadku.
	 Θ- notacja równa - jest to ścisłe ograniczenie określające złożoność olbiczeniową algorytmu, większe niż omega, mniejsze niż big O.
	 Przykład:
			 3n^2≤3n^2+5n+10≤4n^2
			 Ω        ≤    Θ              ≤  O
			 ![[Pasted image 20250713210420.png]]


17. Lista, kolejka i kolejka priorytetowa: ujęcie abstrakcyjne, możliwe implementacje i złożoności:

	Lista to abstrakcyjny typ danych, która przechowuje elementy tego samego typu danych, wykorzystuje pamięć w sposób dynamiczny lub statyczny, zapewnia sekwencyjny dostęp danych, które są liniowo uporządkowane.
	Wyróżniamy listę w postaci:
		Tablicowej - ArrayList, wykorzystujące pamięć w sposób statyczny oraz ma z góry określony rozmiar, który może być niewykorzystany podczas jej istnienia.
		Wiązanej - LinkedList, może być jedno lub dwu kierunkowa, a nawet cykliczna, pierwszy element nazywany głową listy zawiera wskaźnik na drugi element, który zawiera wskaźnik na trzeci itd... ostatni element nazywamy ogonem - tail

	Opearcje na listach i ich złożoność:
		Create - stały
		Append- stały
		Insert - czas liniowy
		Find - czas liniowy
		Delete - czas liniowy
		Makenull - stały


	Kolejka- ADT, który jest sekwencyjny i działa na bazie FIFO, dodajemy nowy element na koniec kolejki, usuwamy element z przodu kolejki.
	Kolejka zawiera informacje o pierwszym elemencie - front i rear - ostatnim, może być przechowywana w formie indeksu np.
	
	Wyróżniamy dwa typy kolejek - Tablicę cykliczną i Listę wiązaną
	
	Operacje na kolejkach:
		Create - Tworzy pusta kolejke, const time
		isEmpty - zwraca informacje, czy kolejka jest pusta, const time
		Enqueue(x) - wstawia x do kolejki - const time
		 Front - odczytuje pierwszy element z kolejki, const time
		 dequeue- usuwa pierwszy element z kolejki i go zwraca, const time

	Implementacja kolejki:
		Na początku zauważmy, że nieefektywną realizacją kolejki w tablicy jest przyjęcie,
		że początek kolejki front będzie zawsze równy 0, a rear będzie indeksem do pierw-
		szego wolnego elementu tablicy.

	 .       Najbardziej efektywnym rozwiązaniem jest reprezentacja kolejki w tablicy cy
		klicznej. Operacje wstawiania i usuwania zwiększają pozycje końca i początku ko-
		lejki o 1 modulo rozmiar tablicy,


	Kolejka priorytetowa to ADT, którego celem jest usuwanie obiektu priorytetu największego/najmniejszego, w zależności od implementacji
		Jej implementacja opiera się o tzw. MIN/MAX Heap, polega na implementacji drzewa binarnego na sorted arrayu. Zachowuje stałą kolejność poprzez insercje na koniec i sprawdzenie poprawności stanu - nowy element zostanie "wybąbelkowany" do góry poprzez zamianę odpowiednich indeksów w tablicy.



18. Algorytmy sortowania - quicksort, mergesort, porównanie, złożoność, algorytmy sortowania bez porównań: zliczanie, kubełkowe, pozycyjne.
	Implementacja quicksorta :

	![[Pasted image 20250714110913.png]]
	Quicksort jest jednym z najpopularniejszych algorytmów sortowania, opiera się o podejście divide and conquer, czyli rozbijania problemu na coraz mniejsze podproblemy w celu wykonania na nich operacji stanu bazowego

	Quicksort ma złożoność średnią i optymistyczną nlogn, oraz złożonosc n^2 w najgorszym przypadku.

	Mergesort:
	![[Pasted image 20250714111213.png]]

	Mergesort - złożoność optymistyczna, średnia i pesymistyczna = nlogn
	Pomimo lepszej złożoności teoretycznej quicksort jest często szybszy, ze wzgledu na dobrą złożoność pamięciową i cacheowanie wykorzystywane przez system.
	![[Pasted image 20250714111418.png]]

### Sortowanie przez zliczanie

Sortowanie przez zliczanie to algorytm stabilny o złożoności O(n + k), gdzie n to liczba elementów, a k to maksymalna wartość klucza. Działa następująco:
1. Tworzy się tablicę pomocniczą C rozmiaru k+1 i zlicza, ile razy każdy klucz występuje w wejściowej tablicy A.  
2. Przekształca się C tak, by C[j] zawierało liczbę elementów ≤ j.  
3. Przechodzi się przez tablicę A od końca do początku i umieszcza każdy element A[i] na właściwej pozycji w wyjściowej tablicy B, dekrementując odpowiednią wartość w C.  
Dzięki temu elementy o równych kluczach zachowują względny porządek (stabilność), a całość wykonuje się w czasie liniowym względem n i k.


```pseudocode
COUNTING_SORT(A, k):
    # A[1..n], wartości w [0..k]
    let C[0..k] być nową tablicą
    for j from 0 to k:
        C[j] ← 0
    for i from 1 to length(A):
        C[A[i]] ← C[A[i]] + 1
    for j from 1 to k:
        C[j] ← C[j] + C[j−1]
    let B[1..length(A)] być nową tablicą
    for i from length(A) down to 1:
        B[C[A[i]]] ← A[i]
        C[A[i]] ← C[A[i]] − 1
    return B

```


Sortowanie kubełkowe to algorytm o oczekiwanej złożoności O(n + m), gdzie n to liczba elementów, a m – liczba kubełków. Zakłada się równomierny rozkład danych (np. wartości z przedziału [0,1)). Działa następująco:
1. Tworzy się n pustych kubełków (list), do których rozdziela się elementy wejściowej tablicy A na podstawie funkcji indeksującej (np. floor(n·A[i])).  
2. Każdy kubełek sortuje się wewnętrznie (najczęściej sortowaniem przez wstawianie — INSERTION_SORT).  
3. Zawartość wszystkich kubełków konkatenacja w kolejności od najmniejszego do największego daje wynik posortowany.  
Algorytm jest bardzo wydajny, gdy dane mają równy rozkład i gdy wewnętrzne sortowanie kubełków jest szybkie.

```
Sortowanie kubełkowe
BUCKET_SORT(A):
    # A[1..n], wartości w [0,1)
    let B[0..n−1] być n pustymi kubełkami (listami)
    for i from 1 to n:
        index ← floor(n * A[i])
        B[index].append(A[i])
    for each bucket in B:
        INSERTION_SORT(bucket)
    return concatenation of all buckets w kolejności
```

Sortowanie kubełkowe to algorytm o oczekiwanej złożoności O(n + m), gdzie n to liczba elementów, a m – liczba kubełków. Zakłada się równomierny rozkład danych (np. wartości z przedziału [0,1)). Działa następująco:
1. Tworzy się n pustych kubełków (list), do których rozdziela się elementy wejściowej tablicy A na podstawie funkcji indeksującej (np. floor(n·A[i])).  
2. Każdy kubełek sortuje się wewnętrznie (najczęściej sortowaniem przez wstawianie — INSERTION_SORT).  
3. Zawartość wszystkich kubełków konkatenacja w kolejności od najmniejszego do największego daje wynik posortowany.  
Algorytm jest bardzo wydajny, gdy dane mają równy rozkład i gdy wewnętrzne sortowanie kubełków jest szybkie.


RADIX sort- sortowanie pozycyjne
```
RADIX_SORT(A, d, b):
    # A[1..n], każdy element ma d cyfr w bazie b
    for i from 1 to d:
        A ← STABLE_COUNTING_SORT_BY_DIGIT(A, i, b)
    return A

STABLE_COUNTING_SORT_BY_DIGIT(A, i, b):
    let C[0..b−1] ← 0
    for each x in A:
        digit ← floor(x / b^(i−1)) mod b
        C[digit] ← C[digit] + 1
    for j from 1 to b−1:
        C[j] ← C[j] + C[j−1]
    let B[1..length(A)]
    for j from length(A) down to 1:
        digit ← floor(A[j] / b^(i−1)) mod b
        B[C[digit]] ← A[j]
        C[digit] ← C[digit] − 1
    return B
```

Sortowanie pozycyjne to metoda stabilnego sortowania kluczy wielocyfrowych (liczb, łańcuchów znaków) w czasie O(d·(n + b)), gdzie d to liczba cyfr (pozycji), a b – baza. Działa według schematu LSD (Least Significant Digit) lub MSD:
1. Dla każdej pozycji i od najmniej znaczącej (i=1) do najbardziej znaczącej (i=d):  
   - Wykonuje się stabilne sortowanie (zwykle COUNTING_SORT) według wartości cyfry na pozycji i.  
   - Dzięki stabilności wcześniejsze porządki wg niższych pozycji są zachowane.  
2. Po d krokach otrzymujemy w pełni posortowaną tablicę.  
Radix Sort jest szczególnie efektywny, gdy d i b są niewielkie w porównaniu do n, i pozwala ominąć logarytmiczny czynnik charakterystyczny dla porównań.  



19.Drzewa BST, porządki przeglądania, wyszukiwanie poprzednika i następnika, usuwanie węzła. Drzewa zrównoważone, AVL, podstawowe operacje i ich złożoność.

# Drzewa BST

BST czyli binary search tree to takie drzewo, ktore zchowuje strukturę uporządkowaną, takie, że:
L>N>R, gdzie L to lewe poddrzewo N to wartość węzła, a R to prawe poddrzewo.

## 1. Porządki przeglądania
- **Preorder (N L R)**  
  1. Odwiedź bieżący węzeł  
  2. Przetwórz lewe poddrzewo  
  3. Przetwórz prawe poddrzewo  
- **Inorder (L N R)**  
  1. Przetwórz lewe poddrzewo  
  2. Odwiedź bieżący węzeł  
  3. Przetwórz prawe poddrzewo  
  > Daje posortowany ciąg kluczy.  
- **Postorder (L R N)**  
  1. Przetwórz lewe poddrzewo  
  2. Przetwórz prawe poddrzewo  
  3. Odwiedź bieżący węzeł  

## 2. Wyszukiwanie poprzednika i następnika
- **Poprzednik (predecessor)**  
  1. Jeśli węzeł ma lewe poddrzewo → największy element w tym poddrzewie  
  2. Inaczej → wspinaj się w górę, aż wejdziesz węzeł będący **prawym** dzieckiem swojego rodzica; ten rodzic to poprzednik  
- **Następnik (successor)**  
  1. Jeśli węzeł ma prawe poddrzewo → najmniejszy element w tym poddrzewie  
  2. Inaczej → wspinaj się w górę, aż wejdziesz węzeł będący **lewym** dzieckiem swojego rodzica; ten rodzic to następnik  

## 3. Usuwanie węzła
- **Przypadki**  
  1. **Liść** → usuń węzeł  
  2. **Jedno dziecko** → zastąp węzeł swoim dzieckiem  
  3. **Dwoje dzieci** → znajdź następnika (lub poprzednika), skopiuj jego wartość do usuwanego węzła, a następnie usuń tego następnika (ma co najwyżej jedno dziecko)  
- **Złożoność**: O(h), gdzie h to wysokość drzewa  
  - W najgorszym przypadku BST: O(n)  
  - Dla drzewa zrównoważonego: O(log n)  

---

# Drzewa zrównoważone

## 1. Drzewa AVL
- **Warunek równowagi**: dla każdego węzła różnica wysokości lewego i prawego poddrzewa ≤ 1  
- **Operacje**  
  - **Wyszukiwanie**: jak w BST (O(log n))  
  - **Wstawianie**:  
    1. Wstaw jak w BST  
    2. Cofając się w górę, aktualizuj wysokości i w razie potrzeby wykonaj rotacje  
  - **Usuwanie**:  
    1. Usuń jak w BST  
    2. Cofając się w górę, aktualizuj wysokości i przywróć równowagę przez rotacje  
- **Rotacje**  
  - **Pojedyncza** (LL, RR)  
  - **Podwójna** (LR, RL)  
- **Złożoność**: O(log n) dla wszystkich podstawowych operacji  

## 2. B-drzewa (rząd m)
- **Struktura**  
  - Każdy węzeł (poza korzeniem) ma od ⌈m/2⌉ do m dzieci  
  - Kluczy w węźle jest o 1 mniej niż dzieci (od ⌈m/2⌉−1 do m−1)  
- **Operacje**  
  - **Wyszukiwanie**: przeglądanie kluczy w węźle + rekurencja do właściwego poddrzewa (O(log n))  
  - **Wstawianie**:  
    1. Wstaw klucz do liścia  
    2. Jeśli liczba kluczy > m−1 → split węzła: mediana idzie do rodzica, pozostałe połówki tworzą dwa węzły  
    3. Rekurencyjnie naprawiaj ewentualne przepełnienia w górę  
  - **Usuwanie**:  
    1. Usuń klucz z węzła (liścia lub wewnętrznego, zastępując go następnikiem/poprzednikiem)  
    2. Jeśli liczba kluczy < ⌈m/2⌉−1 → wypożycz klucz od sąsiada (rotacja) lub połącz węzły (merge) i zaktualizuj rodzica  
- **Złożoność**: O(log n) dla wyszukiwania, wstawiania i usuwania  


## 20. Sposoby konstrukcji algorytmów

### 1. Metoda "dziel i zwyciężaj"
- **Idea**: problem dzielimy na mniejsze podproblemy, rozwiązujemy je niezależnie, a następnie łączymy wyniki.  
- **Przykłady**: sortowanie szybkiego (QuickSort), sortowanie przez scalanie (MergeSort), wyszukiwanie binarne.  
- **Zalety**:  
  - często prostsza rekurencyjna implementacja  
  - dobre wykorzystanie wielordzeniowości (podproblemy można rozwiązywać równolegle)  
  - złożoność często O(n log n) lub lepsza  
- **Wady**:  
  - narzut pamięciowy na rekurencję i dodatkowe struktury (np. bufor scalania)  
  - trudne problemy, w których podproblemy się nakładają – może prowadzić do nadmiarowych obliczeń  

### 2. Programowanie dynamiczne
- **Idea**: podproblemy nakładają się; zapisujemy ich wyniki (memoizacja/tablica) i używamy ponownie zamiast ponownie obliczać.  
- **Przykłady**: obliczanie ciągu Fibonacciego (z zapamiętywaniem), problem plecakowy (0/1 Knapsack), problem najdłuższego wspólnego podciągu (LCS).  
- **Zalety**:  
  - eliminuje powtarzające się obliczenia → znaczące przyspieszenie  
  - często zamienia złożoność wykładniczą na wielomianową  
- **Wady**:  
  - wymaga dodatkowej pamięci na tablice/memoizację  
  - może być trudne do sformułowania stanu i przejść rekurencyjnych  

### 3. Porównanie
- **Nakład obliczeniowy**:  
  - *Dzielenie i zwyciężaj*: czas często O(n log n), ale może powtarzać obliczenia, jeśli podproblemy się nakładają  
  - *Dynamiczne*: zazwyczaj O(n·m) dla problemów z dwoma parametrami, bez nadmiarowych obliczeń  
- **Pamięć**:  
  - *Dz.i.z.*: niższe potrzeby, poza rekurencją i ewentualnymi strukturami pomocniczymi  
  - *DP*: większe potrzeby na przechowywanie tablic i wyników  
- **Łatwość równoleglenia**:  
  - *Dz.i.z.*: dobra (podproblemy niezależne)  
  - *DP*: trudniejsza (zależności między stanami)  

---

## Algorytm zachłanny

### Przykład optymalnego wykorzystania
- **Problem wydawania reszty z monet (monetarny system kanoniczny)**  
  - Dla waluty o nominałach np. [1, 2, 5, 10, 20, 50] algorytm zachłanny (zawsze wziąć największy możliwy nominał) daje zawsze minimalną liczbę monet.  

### Przykład nieoptymalnego wykorzystania
- **Problem wydawania reszty – nietypowy zestaw nominałów**  
  - Dla nominałów [1, 3, 4] i reszty 6 algorytm zachłanny wybierze 4 + 1 + 1 = 3 monety, podczas gdy optymalnie 3 + 3 = 2 monety.  

- **Problem plecakowy 0/1**  
  - Zachłanne dobieranie przedmiotów według najwyższej wartości na jednostkę ciężaru (v/w) nie gwarantuje optymalnego wypełnienia plecaka – należy użyć programowania dynamicznego.  

21. Algorytmy Grafowe
## 21.Algorytmy grafowe

---

### 1. Przeszukiwanie wszerz (BFS)

**Opis:**  
Przeszukiwanie wszerz eksploruje graf warstwami, zaczynając od wierzchołka źródłowego. Najpierw odwiedza wszystkie wierzchołki odległe o 1 krawędź, potem o 2, itd. Przydatne do wyznaczania najkrótszych ścieżek w grafie nieważonym.

**Złożoność:**  
- Czasowa: O(V + E)  
- Pamięciowa: O(V)

```pseudocode
BFS(G, s):
    for each u in G.V:
        u.color ← WHITE; u.d ← ∞; u.π ← NIL
    s.color ← GRAY; s.d ← 0; s.π ← NIL
    Q ← empty queue
    ENQUEUE(Q, s)
    while Q ≠ ∅:
        u ← DEQUEUE(Q)
        for each v in G.adj[u]:
            if v.color = WHITE:
                v.color ← GRAY
                v.d ← u.d + 1
                v.π ← u
                ENQUEUE(Q, v)
        u.color ← BLACK
```
##2. Przeszukiwanie wgłąb(DFS)
```
DFS(G):
    for each u in G.V:
        u.color ← WHITE; u.π ← NIL
    time ← 0
    for each u in G.V:
        if u.color = WHITE:
            DFS-Visit(G, u)

DFS-Visit(G, u):
    time ← time + 1; u.d ← time; u.color ← GRAY
    for each v in G.adj[u]:
        if v.color = WHITE:
            v.π ← u
            DFS-Visit(G, v)
    u.color ← BLACK
    time ← time + 1; u.f ← time
```


## Dijkstra

**Opis:** Znajduje najkrótsze ścieżki od jednego źródła w grafie z nieujemnymi wagami.  
**Złożoność czasowa:**

- z kopcem binarnym: O((V + E) log V)
    
- z kopcem Fibonacciego: O(V log V + E)  
    **Złożoność pamięciowa:** O(V)
```
DIJKSTRA(G, s):
    for each u in G.V:
        u.d ← ∞
        u.π ← NIL
    s.d ← 0
    Q ← G.V               # min-kopiec według u.d
    while Q ≠ ∅ do
        u ← EXTRACT-MIN(Q)
        for each v in G.adj[u] do
            if v.d > u.d + w(u,v) then
                v.d ← u.d + w(u,v)
                v.π ← u
                DECREASE-KEY(Q, v)
```

## Bellman–Ford

**Opis:** Znajduje najkrótsze ścieżki od jednego źródła nawet przy ujemnych wagach (bez ujemnych cykli).  
**Złożoność czasowa:** O(V·E)  
**Złożoność pamięciowa:** O(V)
```
BELLMAN-FORD(G, s):
    for each u in G.V:
        u.d ← ∞
        u.π ← NIL
    s.d ← 0
    for i from 1 to |G.V|−1 do
        for each (u, v) in G.E do
            if v.d > u.d + w(u,v) then
                v.d ← u.d + w(u,v)
                v.π ← u
    # opcjonalnie detekcja ujemnego cyklu:
    for each (u, v) in G.E do
        if v.d > u.d + w(u,v) then
            report "ujemny cykl"

```


## Borůvka

**Opis:** Buduje MST przez wielokrotne łączenie najmniejszych krawędzi z każdego komponentu.  
**Złożoność czasowa:** O(E log V)  
**Złożoność pamięciowa:** O(V)

pseudocode

```
BORUVKA(G):
    A ← ∅
    make each vertex its own component
    while number_of_components > 1 do
        E' ← ∅
        for each component C do
            find lightest edge (u,v) with u in C, v not in C
            E'.append((u,v))
        for each (u,v) in E' do
            if FIND-SET(u) ≠ FIND-SET(v) then
                A.append((u,v))
                UNION(u, v)
    return A

```

## Prim

**Opis:** Rozpoczyna od jednego wierzchołka, iteracyjnie dołącza najtańszą krawędź łączącą drzewo z resztą grafu.  
**Złożoność czasowa:**

- z kopcem binarnym: O((V + E) log V)
    
- z kolejką priorytetową Diala lub bajtowym kopcem: O(E + V log V)  
    **Złożoność pamięciowa:** O(V)

```
PRIM(G, r):
    for each u in G.V:
        u.key ← ∞
        u.π ← NIL
    r.key ← 0
    Q ← G.V               # min-kopiec według u.key
    while Q ≠ ∅ do
        u ← EXTRACT-MIN(Q)
        for each v in G.adj[u] do
            if v in Q and w(u,v) < v.key then
                v.π ← u
                v.key ← w(u,v)
                DECREASE-KEY(Q, v)
```

## Kruskal

**Opis:** Sortuje krawędzie rosnąco i dodaje je, jeśli łączą różne komponenty (DSU).  
**Złożoność czasowa:** O(E log E) = O(E log V)  
**Złożoność pamięciowa:** O(V)

pseudocode

```
KRUSKAL(G):
    A ← ∅
    sort G.E rosnąco wg wagi
    make-set(u) for each u in G.V
    for each (u, v) in G.E do
        if FIND-SET(u) ≠ FIND-SET(v) then
            A.append((u, v))
            UNION(u, v)
    return A

```

## Kolorowanie wierzchołkowe (Greedy)

**Opis:** Zachłannie nadaje najmniejszy możliwy kolor kolejnym wierzchołkom.  
**Złożoność czasowa:** O(V + E)  
**Złożoność pamięciowa:** O(V)

```
GREEDY_VERTEX_COLOR(G):
    for each u in G.V in dowolnej kolejności do
        forbidden ← { v.color | v in G.adj[u] }
        u.color ← smallest k not in forbidden

```

## Kolorowanie krawędziowe (Greedy)

**Opis:** Zachłannie nadaje najmniejszy możliwy kolor kolejnym krawędziom, unikając konfliktów na incydentnych krawędziach.  
**Złożoność czasowa:** O(E + V)  
**Złożoność pamięciowa:** O(E)

```
GREEDY_EDGE_COLOR(G):
    for each edge e = (u, v) in G.E in dowolnej kolejności do
        forbidden ← { e'.color | e' adjacent to u or v }
        e.color ← smallest k not in forbidden

```

22. Najważniejsze algorytmy wyznaczania otoczki wypukłej zbioru punktów w układzie współrzędnych.

## 1. Co to jest „algorytm wyznaczania otoczki wypukłej”

Algorytm wyznaczania otoczki wypukłej dla zbioru punktów w płaszczyźnie to metoda znajdowania najmniejszego wielokąta wypukłego, który zawiera wszystkie te punkty.

- **Otoczka wypukła** to zbiór punktów spośród P, które tworzą wierzchołki tego wielokąta.
    
- Wszystkie pozostałe punkty leżą wewnątrz lub na krawędziach otrzymanego wielokąta.
    
- Zastosowania: grafika komputerowa, analiza kształtów, obliczenia geometryczne.
    

---

## 2. Monotone Chain – krok po kroku pseudokod

1. **Wejście**  
    • P – lista n punktów (x, y)
    
2. **Sortowanie**
    
    1. Posortuj listę P rosnąco po x, a przy równych x – po y.
        
3. **Budowa dolnej otoczki (L)**
    
    1. Utwórz pustą listę L.
        
    2. Dla każdego punktu p z posortowanego P, kolejno:  
        a. Dopóki |L| ≥ 2 i orientacja(L[-2], L[-1], p) ≤ 0, usuń ostatni element z L.  
        b. Dodaj p na koniec L.
        
4. **Budowa górnej otoczki (U)**
    
    1. Utwórz pustą listę U.
        
    2. Dla każdego punktu p z posortowanego P w odwrotnej kolejności:  
        a. Dopóki |U| ≥ 2 i orientacja(U[-2], U[-1], p) ≤ 0, usuń ostatni element z U.  
        b. Dodaj p na koniec U.
        
5. **Scalanie obu łańcuchów**
    
    1. Usuń ostatni punkt z L i ostatni punkt z U (bo są takie same jak punkty startowe).
        
    2. Otrzymaną otoczkę wypukłą H uzyskasz przez połączenie L i U w tej kolejności:  
        • H ← L concatenated with U
        
6. **Wyjście**  
    • H – lista punktów w kolejności zgodnej z obwodem otoczki (zwraca punkty wierzchołkowe).
    

---

### Funkcja pomocnicza

- **orientacja(a, b, c)**  
    Oblicza wartość wyznacznika:
    
    orient = (b.x – a.x)·(c.y – a.y) – (b.y – a.y)·(c.x – a.x)  
    • > 0 → zakręt w lewo  
    • < 0 → zakręt w prawo  
    • = 0 → punkty współliniowe
    

---

> **Złożoność czasowa:**  
> • Sortowanie: O(n log n)  
> • Budowa obu łańcuchów: O(n)  
> **Łącznie:** O(n log n)
> 
> **Pamięciowa:** O(n) (listy L, U i posortowane P)


23. Języki regularne: warunki równoważne definicji- automat, prawa kongruencja, syntaktyczna, wyrażenia regularne. Lemat o pompowaniu kolegi.
## Definicje równoważne języków regularnych

### 1. Automat skończony (DFA/NFA)

- **Deterministyczny automat skończony (DFA)**  
    – pięciotuple \ (Q, Σ, δ, q₀, F)\ , gdzie  
    • Q – skończony zbiór stanów  
    • Σ – alfabet wejściowy  
    • δ : Q × Σ → Q – funkcja przejścia  
    • q₀ ∈ Q – stan startowy  
    • F ⊆ Q – stany akceptujące  
    – akceptuje słowo w ∈ Σ* ⇔ po przetworzeniu w pozostaje w stanie q ∈ F.
    
- **Niedeterministyczny automat skończony (NFA)**  
    – podobnie, ale δ : Q × (Σ ∪ {ε}) → P(Q)  
    – zezwala na przejścia ε i ma wiele możliwych stanów  
    – DFA i NFA rozpoznają dokładnie te same języki.
    

---

### 2. Wyrażenia regularne

- **Składnia**
    
    1. ∅ i ε są wyrażeniami regularnymi.
        
    2. Jeśli a ∈ Σ, to a jest wyrażeniem regularnym.
        
    3. Jeśli R, S są wyrażeniami, to  
        • (R ⋃ S) – alternacja,  
        • (R·S) – konkatenacja,  
        • (R)* – iteracja (Kleene)  
        są wyrażeniami regularnymi.
        
- **Semantyka**  
    – Każde wyrażenie R definiuje język L(R) ⊆ Σ* zgodnie z konstrukcjami:  
    • L(∅) = ∅, L(ε) = {ε}, L(a) = {“a”}  
    • L(R ⋃ S) = L(R) ∪ L(S)  
    • L(R·S) = { xy | x ∈ L(R), y ∈ L(S) }  
    • L(R*) = ⋃_{k≥0} L(R)^k
    

---

### 3. Kongruencja syntaktyczna (Myhill-Nerode)

- **Relacja równoważności ≡ₗ** na Σ*:  
    dla x,y ∈ Σ* mamy x ≡ₗ y ⇔ ∀z ∈ Σ*: xz ∈ L ⇔ yz ∈ L
    
- **Twierdzenie Myhilla-Nerode**  
    L jest regularny ⇔ ≡ₗ ma skończenie wiele klas równoważności.
    
- **Wniosek**  
    • Minimalny DFA dla L ma liczbę stanów równą liczbie klas ≡ₗ.
    

---

## Lemat o pompowaniu dla języków regularnych

1. **Twierdzenie**  
    Jeśli L ⊆ Σ* jest nieskończonym językiem regularnym, to istnieje liczba p ≥ 1 (tzw. długość pompowania) taka, że  
    dla każdego w ∈ L z |w| ≥ p istnieje rozkład  
    w = xyz  
    spełniający:
    
    - |xy| ≤ p
        
    - |y| ≥ 1
        
    - ∀k ≥ 0: x y^k z ∈ L
        
2. **Interpretacja**  
    – Słowo w o długości ≥ p po przejściu przez p+1 stanów DFA musi odwiedzić co najmniej jeden stan dwukrotnie → tam można „pompować” fragment y.
    
3. **Zastosowanie**  
    – Aby pokazać, że język M nie jest regularny, załóż, że jest, wybierz p i spróbuj znaleźć w ∈ M, |w| ≥ p, takie że dla dowolnego rozkładu xyz z warunkami powyżej istnieje k, dla którego x y^k z ∉ M.
    
4. **Przykład dowodu nieregularności**
    
    - L = { aⁿbⁿ | n ≥ 0 }
        
    - Załóż p; wybierz w = a^p b^p
        
    - Każdy rozkład xyz z |xy| ≤ p ⇒ y = a^m dla m ≥ 1
        
    - Dla k=2: x y^2 z = a^{p+m} b^p ma więcej a niż b, więc ∉ L ⇒ sprzeczność.
        

---

## Podsumowanie

- **Automaty**, **wyrażenia regularne** i **klasy ≡ₗ** to trzy równoważne definicje języków regularnych.
    
- **Lemat o pompowaniu** pozwala wykazać nieregularność języka poprzez przeciwdowód.
    
21.Automat minimalny, wybrany algorytm minimalizacji. Automaty deterministyczne i niedeterministyczne (w tym ze stosem); determinizacja.
## Minimalny automat (DFA)

**Opis:**  
Minimalny DFA to najmniejszy (najmniejsza liczba stanów) deterministyczny automat rozpoznający ten sam język co dany DFA. Opiera się na łączeniu równoważnych stanów (Myhill-Nerode).

**Złożoność czasowa:** O(n log n) (Hopcroft)  
**Złożoność pamięciowa:** O(n + m) (n stanów, m przejść)

```pseudocode
HOPCROFT-Minimize(DFA):
    P ← {F, Q \ F}          # podział na akceptujące i nieakceptujące
    W ← {F, Q \ F}
    while W ≠ ∅ do
        A ← any set from W
        remove A from W
        for each symbol c in Σ do
            X ← { q | δ(q, c) ∈ A }
            for each Y in P do
                Y1 ← X ∩ Y
                Y2 ← Y \ X
                if Y1 ≠ ∅ and Y2 ≠ ∅ then
                    replace Y in P by Y1, Y2
                    if Y in W then
                        replace Y in W by Y1, Y2
                    else
                        add smaller of {Y1, Y2} to W
    construct new DFA from blocks in P
```

## Problemy rozstrzygalne i nierozstrzygalne w teorii języków

### 1. Problemy rozstrzygalne  
– istnieje algorytm Turinga, który zawsze zatrzymuje się i poprawnie odpowiada TAK/NIE.  
- **Przynależność (membership)**  
  - Reguł regularnych (DFA/NFA): O(n)  
  - Gramatyk kontekstowo-wolnych (CYK): O(n³)  
- **Pusty język (emptiness)**  
  - Dla DFA/NFA i CFG: decyduje się w czasie wielomianowym  
- **Finiteness (skończoność języka)**  
  - Dla DFA/NFA i CFG: wielomianowo  
- **Inkluzja i równoważność**  
  - Dla regularnych: decyzyjne (poprzez minimalizację i porównanie DFA)  
  - Dla CFG: **nierozstrzygalne**  

### 2. Problemy nierozstrzygalne  
– nie istnieje algorytm, który dla wszystkich instancji zatrzyma się z poprawną odpowiedzią.  
- **Problem stopu (Halting Problem)** dla maszyn Turinga  
- **Problem równoważności CFG**: czy L(G₁)=L(G₂)?  
- **Problem inkluzji CFG**: czy L(G₁)⊆L(G₂)?  
- **Post Correspondence Problem (PCP)**  

---
25.
## Klasy złożoności P, NP, NP-zupełne

### P  
**Opis:** decyzje rozwiązywane deterministycznie w czasie wielomianowym.  
**Definicja:**  
> P = { L | ∃ deterministyczna maszyna Turinga M i wielomian p(n) takie, że M decyduje L w czasie O(p(n)) }  
**Przykłady:** przeszukiwanie BFS/DFS, mnożenie macierzy, sortowanie przeglądane, sprawdzanie przynależności w DFA.

### NP  
**Opis:** problemy, dla których „TAK” można zweryfikować w czasie wielomianowym przy użyciu dowodu (certyfikatu).  
**Definicja:**  
> NP = { L | ∃ niedeterministyczna maszyna Turinga M działająca w czasie wielomianowym, która akceptuje L }  
– równoważnie: ∃ deterministyczna maszyna weryfikująca certyfikat w wielomianowym czasie.  
**Przykłady:** SAT, CLIQUE, Hamiltonian Path.

### NP-zupełne  
**Opis:** najtrudniejsze problemy w NP; każdy problem z NP można zredukować do nich w czasie wielomianowym.  
**Definicja:** L jest NP-zupełne ⇔  
1. L ∈ NP  
2. ∀ L' ∈ NP: L' ≤ₚ L (wielomianowa redukcja)  
**Przykłady:** SAT (Twierdzenie Cooka), 3-SAT, Vertex Cover, Traveling Salesman Decision.

---

## Zależności między klasami

- P ⊆ NP ⊆ PSPACE ⊆ …  
- Jeśli ∃ choć jeden NP-zupełny algorytm w P ⇔ P = NP.  
- Hipoteza P ≠ NP ⇔ P jest ściśle mniejsze od NP.

---

## Hipoteza P vs NP

- **Pytanie otwarte:** Czy każdy problem, którego rozwiązanie da się zweryfikować w czasie wielomianowym, da się też rozwiązać w czasie wielomianowym?  
- **Implikacje:**  
  - P = NP → większość problemów kombinatorycznych miałaby efektywne rozwiązania  
  - P ≠ NP → są problemy w NP, których nie da się rozwiązać szybciej niż w czasie wykładniczym  
- **Status:** nierozstrzygnięte od 1971; jedno z najważniejszych pytań w informatyce teoretycznej i matematyce.  


26. Chomsky
## Hierarchia Chomsky’ego

- **Typ 0** (rekurencyjnie przeliczalne)  
    – akceptowane przez niedeterministyczną maszynę Turinga.
    
- **Typ 1** (kontekstowo-wrażliwe)  
    – akceptowane przez liniowo ograniczone PDA (LBA).
    
- **Typ 2** (bezkontekstowe)  
    – akceptowane przez niedeterministyczne PDA.
    
- **Typ 3** (regularne)  
    – akceptowane przez DFA/NFA lub opisane wyrażeniami regularnymi.
    

---

## Zamkniętość klas języków

### Typ 3: języki regularne

**Operacje boolowskie**

- suma (∪): ✓
    
- przekrój (∩): ✓
    
- dopełnienie: ✓
    
- różnica: ✓
    

**Inne operacje**

- konkatenacja: ✓
    
- gwiazdka Kleene (L*): ✓
    
- homomorfizm: ✓
    
- odwrotny homomorfizm: ✓
    
- substytucja: ✓
    
- odwrócenie (reversal): ✓
    
- iloraz lewostronny/prawo (L∕R): ✓
    

---

### Typ 2: języki bezkontekstowe

**Operacje boolowskie**

- suma (∪): ✓
    
- przekrój (∩) z dowolnym CF: ✗
    
- przekrój (∩) z regularnym: ✓
    
- dopełnienie: ✗
    
- różnica: ✗
    

**Inne operacje**

- konkatenacja: ✓
    
- gwiazdka Kleene (L*): ✓
    
- homomorfizm: ✓
    
- odwrotny homomorfizm: ✓
    
- substytucja: ✓
    
- odwrócenie (reversal): ✓
    
- iloraz przez regularny (L∕R, R∖L): ✓
    

---

### Typ 1: języki kontekstowo-wrażliwe

**Operacje boolowskie**

- suma (∪): ✓
    
- przekrój (∩): ✓
    
- dopełnienie: ✓
    
- różnica: ✓
    

**Inne operacje**

- konkatenacja: ✓
    
- gwiazdka Kleene (L*): ✓
    
- homomorfizm (nie-kasujący): ✓
    
- odwrotny homomorfizm: ✓
    
- substytucja (z językami CS): ✓
    
- odwrócenie (reversal): ✓
    
- iloraz lewostronny/prawo: ✓
    

---

### Typ 0: języki rekurencyjnie przeliczalne

**Operacje boolowskie**

- suma (∪): ✓
    
- przekrój (∩): ✓
    
- dopełnienie: ✗
    
- różnica: ✗
    

**Inne operacje**

- konkatenacja: ✓
    
- gwiazdka Kleene (L*): ✓
    
- homomorfizm: ✓
    
- odwrotny homomorfizm: ✓
    
- substytucja: ✓
    
- odwrócenie (reversal): ✓
    
- iloraz lewostronny/prawo: ✓
    

---

**Uwagi:**

- „✗” oznacza brak zamknięcia w ogólności (możliwe wyjątki przy dodatkowych ograniczeniach).
    
- dla CF i CS niektóre operacje (np. przekrój) stają się zamknięte, gdy jeden operand jest z klasy niższej (zwykle regularnej).