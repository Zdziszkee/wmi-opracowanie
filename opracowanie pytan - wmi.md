
# Matematyczne podstawy informatyki
#### 1. Elementy teorii mnogości: relacje równoważności, relacje porządku. Metody dowodzenia twierdzeń.
 1. Relacje równoważności
	
	Relacja równoważności to relacja binarna na zbiorze, która spełnia trzy podstawowe własności: zwrotność, symetrię i przechodniość. Formalnie, dla zbioru $A$ relacja $R \subseteq A \times A$ jest relacją równoważności, jeśli:
	
	- **Zwrotność**: Dla każdego $a \in A$, zachodzi $(a, a) \in R$.
	- **Symetria**: Jeśli $(a, b) \in R$, to $(b, a) \in R$.
	- **Przechodniość**: Jeśli $(a, b) \in R$ oraz $(b, c) \in R$, to $(a, c) \in R$.
	
	### Przykłady relacji równoważności
	
	1. Relacja równości na zbiorze liczb rzeczywistych ($\mathbb{R}$): $a = b$.
	2. Relacja „bycia kongruentnym modulo $n$” na zbiorze liczb całkowitych ($\mathbb{Z}$): $a \equiv b \pmod{n}$, jeśli $n$ dzieli $(a - b)$.
	3. Relacja „bycia równoległym” na zbiorze prostych w płaszczyźnie euklidesowej.
	
	### Klasy równoważności
	
	Relacja równoważności dzieli zbiór $A$ na rozłączne podzbiory zwane **klasami równoważności**. Klasą równoważności elementu $a \in A$ jest zbiór:  
	$[a] = { b \in A \mid (a, b) \in R }$.  
	Zbiór wszystkich klas równoważności nazywany jest **zbiorem ilorazowym** $A/R$.
	
	### Twierdzenie o klasach równoważności
	
	Każda relacja równoważności na zbiorze $A$ indukuje podział zbioru $A$ na rozłączne klasy równoważności, takie że ich suma pokrywa cały zbiór $A$.
 2. Relacje porządku
	
	Relacja porządku to relacja binarna na zbiorze, która jest zwrotna, antysymetryczna i przechodnia. Wyróżniamy dwa główne typy relacji porządku:
	
	### Relacja częściowego porządku
	
	Relacja $R \subseteq A \times A$ jest relacją częściowego porządku, jeśli:
	
	- **Zwrotność**: Dla każdego $a \in A$, $(a, a) \in R$.
	- **Antysymetria**: Jeśli $(a, b) \in R$ i $(b, a) \in R$, to $a = b$.
	- **Przechodniość**: Jeśli $(a, b) \in R$ oraz $(b, c) \in R$, to $(a, c) \in R$.
	
	### Przykłady relacji częściowego porządku
	
	1. Relacja „mniejsze lub równe” ($\leq$) na zbiorze liczb rzeczywistych.
	2. Relacja „dzielności” na zbiorze liczb naturalnych: $a \mid b$, jeśli $a$ dzieli $b$.
	3. Relacja zawierania ($\subseteq$) na zbiorze potęgowym $\mathcal{P}(A)$.
	
	### Relacja liniowego porządku
	
	Relacja częściowego porządku jest liniowa (całkowita), jeśli dla każdych $a, b \in A$, zachodzi $(a, b) \in R$ lub $(b, a) \in R$. Przykład: relacja $\leq$ na $\mathbb{R}$.
	
	### Elementy maksymalne i minimalne
	
	- **Element maksymalny**: Element $m \in A$, taki że nie istnieje $a \in A$, $a \neq m$, dla którego $(m, a) \in R$.
	- **Element minimalny**: Element $m \in A$, taki że nie istnieje $a \in A$, $a \neq m$, dla którego $(a, m) \in R$.
 3. Metody dowodzenia twierdzeń
	
	W teorii mnogości stosuje się różne metody dowodzenia twierdzeń, które pozwalają na formalne uzasadnienie własności relacji i innych struktur. Poniżej przedstawiono najczęściej stosowane metody:
	
	### 3.1. Dowód wprost
	
	Polega na bezpośrednim wykazaniu, że założenia implikują tezę twierdzenia, stosując definicje i wcześniej udowodnione twierdzenia.
	
	**Przykład**: Udowodnić, że relacja równości na zbiorze $A$ jest relacją równoważności.
	
	- **Zwrotność**: Dla każdego $a \in A$, $a = a$, więc $(a, a) \in R$.
	- **Symetria**: Jeśli $a = b$, to $b = a$, więc $(b, a) \in R$.
	- **Przechodniość**: Jeśli $a = b$ i $b = c$, to $a = c$, więc $(a, c) \in R$.
	
	### 3.2. Dowód przez sprzeczność
	
	Zakładamy, że teza twierdzenia jest fałszywa, i pokazujemy, że prowadzi to do sprzeczności z założeniami.
	
	**Przykład**: Udowodnić, że w liniowym porządku element maksymalny, jeśli istnieje, jest jednoznaczny.
	
	- Załóżmy, że istnieją dwa różne elementy maksymalne $m_1, m_2 \in A$, $m_1 \neq m_2$.
	- Ponieważ porządek jest liniowy, musi zachodzić $m_1 \leq m_2$ lub $m_2 \leq m_1$.
	- Jeśli $m_1 \leq m_2$, to $m_1$ nie jest maksymalny (bo $m_2 > m_1$), co prowadzi do sprzeczności.
	- Analogicznie dla $m_2 \leq m_1$. Zatem element maksymalny jest jednoznaczny.
	
	### 3.3. Dowód przez indukcję
	
	Stosowany w przypadku twierdzeń dotyczących zbiorów uporządkowanych, np. liczb naturalnych. Polega na:
	
	1. Pokazaniu, że twierdzenie jest prawdziwe dla przypadku bazowego.
	2. Założeniu, że twierdzenie jest prawdziwe dla pewnego $n$, i wykazaniu, że jest prawdziwe dla $n+1$.
	
	**Przykład**: Udowodnić, że w skończonym zbiorze z relacją częściowego porządku istnieje element minimalny.
	
	- Rozważmy zbiór $A = {a_1, a_2, \ldots, a_n}$.
	- **Baza indukcji**: Dla $|A| = 1$, zbiór ma jeden element, który jest minimalny.
	- **Krok indukcyjny**: Załóżmy, że dla zbioru $A$ o $n$ elementach istnieje element
#### 2. Metody numeryczne: rozwiązywania równań nieliniowych (metoda Newtona) oraz układów równań liniowych (metoda Gaussa, metoda Gaussa-Seidla) 

1. Rozwiązywanie równań nieliniowych: Metoda Newtona
	
	Metoda Newtona (nazywana także metodą Newtona-Raphsona) jest iteracyjną metodą numeryczną służącą do znajdowania przybliżonych rozwiązań równań nieliniowych postaci $f(x) = 0$, gdzie $f$ jest funkcją różniczkowalną.
	
	### Zasada działania
	
	Metoda Newtona opiera się na liniowym przybliżeniu funkcji $f(x)$ w okolicy punktu $x_n$ za pomocą szeregu Taylora. Przyjmując, że $x_{n+1}$ jest przybliżonym rozwiązaniem, mamy:  
	$x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)},$  
	gdzie $f'(x_n)$ to pochodna funkcji $f$ w punkcie $x_n$.
	
	### Algorytm
	
	1. Wybierz początkowe przybliżenie $x_0$.
	2. Oblicz kolejne przybliżenie: $x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}$.
	3. Powtarzaj krok 2, aż spełniony zostanie warunek stopu, np. $|x_{n+1} - x_n| < \epsilon$ lub $|f(x_{n+1})| < \epsilon$, gdzie $\epsilon$ jest zadaną dokładnością.
	4. Jeśli $f'(x_n) = 0$, metoda może zawieść (trzeba wybrać inne $x_0$).
	
	### Przykład
	
	Rozwiążmy równanie $f(x) = x^2 - 2 = 0$ (przybliżenie pierwiastka $\sqrt{2}$).
	
	- Pochodna: $f'(x) = 2x$.
	- Start: $x_0 = 1$.
	- Iteracje:
	    - $x_1 = x_0 - \frac{f(x_0)}{f'(x_0)} = 1 - \frac{1^2 - 2}{2 \cdot 1} = 1 - \frac{-1}{2} = 1.5$,
	    - $x_2 = 1.5 - \frac{1.5^2 - 2}{2 \cdot 1.5} = 1.5 - \frac{0.25}{3} \approx 1.4167$,
	    - $x_3 \approx 1.4142$ (zbliża się do $\sqrt{2} \approx 1.414213562$).
	
	### Własności
	
	- **Zalety**: Szybka zbieżność (kwadratowa) w pobliżu pierwiastka, jeśli $f'(x) \neq 0$ i funkcja jest dostatecznie gładka.
	- **Wady**: Wrażliwość na wybór $x_0$; może nie zbiec, jeśli $f'(x_n)$ jest bliska zeru lub funkcja ma ekstremum lokalne.
2. Rozwiązywanie układów równań liniowych
	1. Metoda Gaussa (eliminacja Gaussa)
		Metoda Gaussa to bezpośrednia metoda rozwiązywania układów równań liniowych postaci $Ax = b$, gdzie $A$ jest macierzą współczynników, $x$ wektorem niewiadomych, a $b$ wektorem wyrazów wolnych.
		
		### Algorytm
		
		1. **Eliminacja w przód**:
		    - Przekształć macierz $A$ do postaci trójkątnej górnej za pomocą operacji elementarnych (dodawanie wielokrotności jednego wiersza do drugiego).
		    - Dla macierzy rozszerzonej $[A|b]$, eliminuj elementy pod przekątną, aby uzyskać macierz trójkątną.
		2. **Rozwiązanie wstecz**:
		    - Rozwiązuj układ trójkątny od dołu do góry, obliczając wartości niewiadomych $x_n, x_{n-1}, \ldots, x_1$.
		
		### Przykład
		Rozwiążmy układ: $$
		
		\begin{cases}
		
		2x_1 + x_2 - x_3 = 8, \\
		
		-x_1 + 3x_2 + 2x_3 = -1, \\
		
		x_1 - x_2 + 3x_3 = 9.
		
		\end{cases}
		
		$$
		Macierz rozszerzona: $$ \begin{bmatrix}
		
		2 & 1 & -1 & 8 \\
		
		-1 & 3 & 2 & -1 \\
		
		1 & -1 & 3 & 9
		
		\end{bmatrix} $$
		  
		- Eliminacja w przód:
		    - Wiersz 2: dodaj wiersz 1 pomnożony przez $\frac{1}{2}$, aby wyeliminować $-x_1$.
		    - Wiersz 3: odejmij wiersz 1 pomnożony przez $\frac{1}{2}$.
		    - Po przekształceniach: macierz trójkątna górna.
		- Rozwiązanie wstecz: oblicz $x_3$, potem $x_2$, $x_1$.  
		    Rozwiązanie: $x_1 = 2$, $x_2 = 1$, $x_3 = 3$.
		
		### Własności
		
		- **Zalety**: Prosta i efektywna dla małych układów; dokładna dla macierzy dobrze uwarunkowanych.
		- **Wady**: Wrażliwa na błędy zaokrągleń; wymaga pivotowania dla macierzy źle uwarunkowanych.
	2. Metoda Gaussa-Seidla
		
		Metoda Gaussa-Seidla to iteracyjna metoda rozwiązywania układów równań liniowych, szczególnie skuteczna dla macierzy rzadkich lub diagonalnie dominujących.
		
		### Algorytm
		
		Dla układu $Ax = b$, przepisujemy każde równanie wავ
		
		System: Metoda Gaussa-Seidla wymaga przepisania równań w postaci iteracyjnej. Dla równania $a_{ii}x_i + \sum_{j \neq i} a_{ij}x_j = b_i$, wyznaczamy $x_i$:  
		$x_i^{(k+1)} = \frac{1}{a_{ii}} \left( b_i - \sum_{j < i} a_{ij}x_j^{(k+1)} - \sum_{j > i} a_{ij}x_j^{(k)} \right),$  
		gdzie $x^{(k)}$ to przybliżenie z $k$-tej iteracji, a $x^{(k+1)}$ to nowe przybliżenie. W metodzie Gaussa-Seidla używamy najnowszych wartości $x_j^{(k+1)}$ dla $j < i$, co przyspiesza zbieżność w porównaniu do metody Jacobiego.
		
		### Przykład
		
		Rozważmy ten sam układ co w metodzie Gaussa:   $$ \begin{cases} 2x_1 + x_2 - x_3 = 8, \\ -x_1 + 3x_2 + 2x_3 = -1, \\ x_1 - x_2 + 3x_3 = 9. \end{cases} $$
		  
		Przepisujemy równania:
		
		- $x_1 = \frac{8 - x_2 + x_3}{2}$,
		- $x_2 = \frac{-1 + x_1 - 2x_3}{3}$,
		- $x_3 = \frac{9 - x_1 + x_2}{3}$.  
		    Start: $x_1^{(0)} = x_2^{(0)} = x_3^{(0)} = 0$.  
		    Iteracje:
		- $x_1^{(1)} = \frac{8 - 0 + 0}{2} = 4$,
		- $x_2^{(1)} = \frac{-1 + 4 - 2 \cdot 0}{3} = 1$,
		- $x_3^{(1)} = \frac{9 - 4 + 1}{3} = 2$.  
		    Powtarzamy, aż $|x^{(k+1)} - x^{(k)}| < \epsilon$. Rozwiązanie zbiega do $x_1 \approx 2$, $x_2 \approx 1$, $x_3 \approx 3$.
		
		### Własności
		
		- **Zalety**: Prosta implementacja; skuteczna dla macierzy diagonalnie dominujących; wymaga mniej pamięci niż metoda Gaussa.
		- **Wady**: Zbiega tylko dla pewnych klas macierzy (np. diagonalnie dominujących); wolniejsza zbieżność niż metoda Gaussa dla małych układów.
3. Zastosowania
	- **Metoda Newtona**: Używana w optymalizacji, analizie numerycznej, rozwiązywaniu równań w fizyce i inżynierii.
	- **Metoda Gaussa**: Stosowana w systemach liniowych w inżynierii, ekonomii, analizie danych.
	- **Metoda Gaussa-Seidla**: Popularna w symulacjach numerycznych, np. w równaniach różniczkowych cząstkowych.
#### 3. Metody numeryczne: wartości i wektory własne macierzy, interpolacja wielomianowa.

1. Wartości i wektory własne macierzy
	
	Wartości własne i wektory własne macierzy są kluczowymi pojęciami w algebrze liniowej, mającymi szerokie zastosowanie w analizie numerycznej, np. w analizie stabilności, przetwarzaniu sygnałów czy mechanice.
	
	### Definicje
	
	Dla macierzy kwadratowej $A$ rozmiaru $n \times n$, liczba $\lambda$ jest **wartością własną** (eigenvalue), jeśli istnieje niezerowy wektor $v$, zwany **wektorem własnym** (eigenvector), taki że:  
	$Av = \lambda v.$  
	Równanie to można przepisać jako:  
	$(A - \lambda I)v = 0,$  
	gdzie $I$ to macierz jednostkowa. Aby równanie miało niezerowe rozwiązanie $v$, musi być spełniony warunek:  
	$\det(A - \lambda I) = 0.$  
	Równanie $\det(A - \lambda I) = 0$ nazywane jest **równaniem charakterystycznym**, a jego pierwiastki to wartości własne $\lambda$.

2. Metody obliczania wartości i wektorów własnych
	
	1. Metoda potęgowa
		Metoda potęgowa jest iteracyjną metodą do znajdowania dominującej wartości własnej (o największej wartości bezwzględnej) i odpowiadającego jej wektora własnego.
		
		**Algorytm**:
		
		1. Wybierz początkowy wektor $v_0$ (np. losowy, niezerowy).
		2. Iteracyjnie obliczaj: $v_{k+1} = \frac{Av_k}{|Av_k|}$, gdzie $|\cdot|$ to norma wektora (np. norma euklidesowa).
		3. Oblicz przybliżenie wartości własnej: $\lambda_k = \frac{v_k^T A v_k}{v_k^T v_k}$ (przybliżenie Rayleigha).
		4. Powtarzaj, aż $|v_{k+1} - v_k| < \epsilon$ lub $|\lambda_{k+1} - \lambda_k| < \epsilon$, gdzie $\epsilon$ to zadana dokładność.
		
		**Przykład**:  
		Rozważmy macierz:  
		$$  
		\begin{bmatrix}  
		2 & 1 \\  
		1 & 2  \\
		\end{bmatrix}  
		$$
		
		- Start: $v_0 = \begin{bmatrix} 1 \ 0 \end{bmatrix}$.
		- Iteracja 1: $Av_0 = \begin{bmatrix} 2 \ 1 \end{bmatrix}$, norma $|Av_0| = \sqrt{5}$, więc $v_1 = \frac{1}{\sqrt{5}} \begin{bmatrix} 2 \ 1 \end{bmatrix}$.
		- Oblicz $\lambda_1 \approx v_1^T A v_1$. Po kilku iteracjach zbiega do $\lambda = 3$, a wektor własny do $\begin{bmatrix} \frac{1}{\sqrt{2}} \ \frac{1}{\sqrt{2}} \end{bmatrix}$.
		**Własności**:
		- **Zalety**: Prosta implementacja, skuteczna dla macierzy z dominującą wartością własną.
		- **Wady**: Nie działa, jeśli wartości własne mają tę samą wartość bezwzględną; wolna zbieżność dla bliskich wartości własnych.
	
	#### 1.2. Metoda QR
	
	Metoda QR jest bardziej ogólna i pozwala znaleźć wszystkie wartości własne macierzy. Wykorzystuje rozkład QR macierzy.
	
	**Algorytm**:
	
	2. Rozłóż macierz $A_0 = A$ na $A_0 = Q_0 R_0$, gdzie $Q_0$ jest macierzą ortogonalną, a $R_0$ trójkątną górną.
	3. Oblicz $A_1 = R_0 Q_0$.
	4. Powtarzaj: $A_k = Q_k R_k$, $A_{k+1} = R_k Q_k$, aż $A_k$ zbiega do macierzy trójkątnej, której elementy na przekątnej to wartości własne.
	5. Wektory własne można uzyskać przez rozwiązanie $(A - \lambda_i I)v_i = 0$ dla każdej wartości własnej $\lambda_i$.
	
	**Własności**:
	
	- **Zalety**: Znajduje wszystkie wartości własne; skuteczna dla macierzy symetrycznych.
	- **Wady**: Wymaga więcej obliczeń niż metoda potęgowa; złożoność obliczeniowa $O(n^3)$ na iterację.
	
	### Zastosowania
	
	- Analiza drgań mechanicznych (np. wartości własne określają częstotliwości własne).
	- Kompresja danych (np. PCA – analiza głównych składowych).
	- Rozwiązywanie układów równań różniczkowych.

 3. Interpolacja wielomianowa
	Interpolacja wielomianowa polega na znalezieniu wielomianu, który przechodzi przez zadany zbiór punktów $(x_i, y_i)$, gdzie $i = 0, 1, \ldots, n$. Jest to przydatne w aproksymacji funkcji, modelowaniu danych czy numerycznym różniczkowaniu.
	1. Interpolacja Lagrange’a
		Metoda Lagrange’a konstruuje wielomian interpolacyjny wprost, bez konieczności rozwiązywania układów równań.
		
		**Wzór**:  
		Dla punktów $(x_0, y_0), (x_1, y_1), \ldots, (x_n, y_n)$, wielomian interpolacyjny $P(x)$ ma postać:  
		$P(x) = \sum_{i=0}^n y_i L_i(x),$  
		gdzie $L_i(x)$ to wielomiany bazowe Lagrange’a:  
		$L_i(x) = \prod_{j \neq i} \frac{x - x_j}{x_i - x_j}.$
		
		**Przykład**:  
		Dane punkty: $(0, 1)$, $(1, 0)$, $(2, 3)$.
		
		- Wielomiany bazowe:
		    - $L_0(x) = \frac{(x-1)(x-2)}{(0-1)(0-2)} = \frac{(x-1)(x-2)}{2}$,
		    - $L_1(x) = \frac{(x-0)(x-2)}{(1-0)(1-2)} = \frac{x(x-2)}{-1} = -x(x-2)$,
		    - $L_2(x) = \frac{(x-0)(x-1)}{(2-0)(2-1)} = \frac{x(x-1)}{2}$.
		- Wielomian: $P(x) = 1 \cdot \frac{(x-1)(x-2)}{2} + 0 \cdot (-x(x-2)) + 3 \cdot \frac{x(x-1)}{2}$.
		- Po uproszczeniu: $P(x) = 2x^2 - 3x + 1$.
		
		**Własności**:
		
		- **Zalety**: Prosta konstrukcja; nie wymaga rozwiązywania układów równań.
		- **Wady**: Wysoka złożoność obliczeniowa ($O(n^2)$) dla wielu punktów; niestabilność dla dużych $n$ (zjawisko Rungego).
	2. Interpolacja Newtona
		Metoda Newtona używa różnic dzielonych, co ułatwia dodawanie nowych punktów do interpolacji.
		
		**Wzór**:  
		Wielomian Newtona ma postać:  
		$P(x) = \sum_{i=0}^n f[x_0, \ldots, x_i] \prod_{j=0}^{i-1} (x - x_j),$  
		gdzie $f[x_0, \ldots, x_i]$ to różnice dzielone zdefiniowane rekurencyjnie:
		
		- $f[x_i] = y_i$,
		- $f[x_i, \ldots, x_{i+k}] = \frac{f[x_{i+1}, \ldots, x_{i+k}] - f[x_i, \ldots, x_{i+k-1}]}{x_{i+k} - x_i}$.
		
		**Przykład**:  
		Te same punkty: $(0, 1)$, $(1, 0)$, $(2, 3)$.
		
		- Różnice dzielone:
		    - $f[0] = 1$, $f[1] = 0$, $f[2] = 3$,
		    - $f[0,1] = \frac{0-1}{1-0} = -1$, $f[1,2] = \frac{3-0}{2-1} = 3$,
		    - $f[0,1,2] = \frac{3-(-1)}{2-0} = 2$.
		- Wielomian: $P(x) = 1 + (-1)(x-0) + 2(x-0)(x-1) = 2x^2 - 3x + 1$.
		
		**Własności**:
		
		- **Zalety**: Efektywne dodawanie nowych punktów; stabilniejsze dla dużych $n$ niż Lagrange.
		- **Wady**: Wymaga obliczania różnic dzielonych; może być niestabilne dla źle uwarunkowanych punktów.
		
		### Zastosowania
		
		- Aproksymacja funkcji w symulacjach numerycznych.
		- Rekonstrukcja sygnałów w przetwarzaniu danych.
		- Numeryczne różniczkowanie i całkowanie oparte na wielomianach interpolacyjnych.
		
		## 3. Uwagi końcowe
		
		- **Wartości i wektory własne**: Metoda potęgowa jest prosta dla dominujących wartości własnych, ale metoda QR jest bardziej uniwersalna. Wybór metody zależy od struktury macierzy i wymagań obliczeniowych.
		- **Interpolacja wielomianowa**: Metoda Lagrange’a jest intuicyjna, ale Newtona jest bardziej elastyczna przy dodawaniu punktów. Należy uważać na zjawisko Rungego przy interpolacji wysokiego stopnia.
#### 4.Rachunek prawdopodobieństwa: zmienne losowe dyskretne oraz ciągłe, definicje i najważniejsze rozkłady; łańcuchy Markowa, rozkład stacjonarny. 

1. Zmienne losowe
	
	Zmienna losowa to funkcja $X: \Omega \to \mathbb{R}$ określona na przestrzeni probabilistycznej $(\Omega, \mathcal{F}, P)$, gdzie $\Omega$ to przestrzeń próbek, $\mathcal{F}$ to sigma-algebra, a $P$ to miara prawdopodobieństwa. Zmienne losowe dzielimy na **dyskretne** i **ciągłe**.

2. Zmienne losowe dyskretne
	
	Zmienna losowa $X$ jest dyskretna, jeśli jej zbiór wartości jest skończony lub przeliczalny. Charakteryzuje ją **funkcja masy prawdopodobieństwa** (PMF, ang. probability mass function):  
	$p_X(x) = P(X = x),$  
	gdzie $\sum_{x \in \text{range}(X)} p_X(x) = 1$.

3. Najważniejsze rozkłady dyskretne
	
	1. **Rozkład Bernoulliego**:
	    
	    - Opis: Modeluje eksperyment z dwoma możliwymi wynikami (sukces/porażka).
	    - PMF: $p_X(x) = p^x (1-p)^{1-x}$, dla $x \in {0, 1}$, gdzie $p$ to prawdopodobieństwo sukcesu.
	    - Wartość oczekiwana: $E[X] = p$.
	    - Wariancja: $\text{Var}(X) = p(1-p)$.
	    - Zastosowanie: Modelowanie bitów w systemach cyfrowych, testy A/B.
	2. **Rozkład Poissona**:
	    
	    - Opis: Modeluje liczbę zdarzeń w stałym interwale czasu lub przestrzeni.
	    - PMF: $p_X(x) = \frac{\lambda^x e^{-\lambda}}{x!}$, dla $x = 0, 1, 2, \ldots$, gdzie $\lambda > 0$ to średnia liczba zdarzeń.
	    - Wartość oczekiwana: $E[X] = \lambda$.
	    - Wariancja: $\text{Var}(X) = \lambda$.
	    - Zastosowanie: Analiza ruchu sieciowego, kolejki w systemach komputerowych.
	3. **Rozkład geometryczny**:
	    
	    - Opis: Modeluje liczbę prób do pierwszego sukcesu w niezależnych próbach Bernoulliego.
	    - PMF: $p_X(x) = (1-p)^{x-1} p$, dla $x = 1, 2, \ldots$, gdzie $p$ to prawdopodobieństwo sukcesu.
	    - Wartość oczekiwana: $E[X] = \frac{1}{p}$.
	    - Wariancja: $\text{Var}(X) = \frac{1-p}{p^2}$.
	    - Zastosowanie: Modelowanie czasu oczekiwania na zdarzenie w algorytmach.
	
4. Zmienne losowe ciągłe
	
	Zmienna losowa $X$ jest ciągła, jeśli jej wartości należą do nieprzeliczalnego zbioru (np. przedziału w $\mathbb{R}$). Charakteryzuje ją **gęstość prawdopodobieństwa** (PDF, ang. probability density function) $f_X(x)$, taka że:  
	$P(a \leq X \leq b) = \int_a^b f_X(x) , dx,$  
	gdzie $\int_{-\infty}^\infty f_X(x) , dx = 1$.

5. Najważniejsze rozkłady ciągłe
	
	1. **Rozkład jednostajny**:
	    
	    - Opis: Modeluje zmienną losową o równym prawdopodobieństwie na przedziale $[a, b]$.
	    - PDF: $f_X(x) = \frac{1}{b-a}$ dla $x \in [a, b]$, inaczej $0$.
	    - Wartość oczekiwana: $E[X] = \frac{a+b}{2}$.
	    - Wariancja: $\text{Var}(X) = \frac{(b-a)^2}{12}$.
	    - Zastosowanie: Generowanie losowych liczb w symulacjach (np. algorytmy Monte Carlo).
	2. **Rozkład normalny (Gaussa)**:
	    
	    - Opis: Modeluje zmienne losowe o symetrycznym rozkładzie wokół średniej.
	    - PDF: $f_X(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$, gdzie $\mu$ to średnia, $\sigma^2$ to wariancja.
	    - Wartość oczekiwana: $E[X] = \mu$.
	    - Wariancja: $\text{Var}(X) = \sigma^2$.
	    - Zastosowanie: Analiza błędów pomiarowych, uczenie maszynowe (np. rozkład cech).
	3. **Rozkład wykładniczy**:
	    
	    - Opis: Modeluje czas oczekiwania między zdarzeniami w procesie Poissona.
	    - PDF: $f_X(x) = \lambda e^{-\lambda x}$ dla $x \geq 0$, gdzie $\lambda > 0$ to parametr intensywności.
	    - Wartość oczekiwana: $E[X] = \frac{1}{\lambda}$.
	    - Wariancja: $\text{Var}(X) = \frac{1}{\lambda^2}$.
	    - Zastosowanie: Modelowanie czasów życia w systemach niezawodności, kolejki w sieciach.

6. Łańcuchy Markowa
	Łańcuch Markowa to model stochastyczny opisujący sekwencję stanów, w której prawdopodobieństwo przejścia do kolejnego stanu zależy tylko od bieżącego stanu (własność Markowa). Formalnie, dla dyskretnego łańcucha Markowa z przestrzenią stanów $S = {s_1, s_2, \ldots}$:  
	$P(X_{n+1} = s_j \mid X_n = s_i, X_{n-1}, \ldots, X_0) = P(X_{n+1} = s_j \mid X_n = s_i)$.
	
	### 2.1. Macierz przejścia
	
	Łańcuch Markowa z czasem dyskretnym (DTMC, ang. Discrete-Time Markov Chain) jest określony przez macierz przejścia $P$, gdzie:  
	$P_{ij} = P(X_{n+1} = s_j \mid X_n = s_i),$  
	a $\sum_{j} P_{ij} = 1$ dla każdego $i$ (macierz stochastyczna).
	
	**Przykład**:  
	Rozważmy łańcuch z trzema stanami ${1, 2, 3}$ i macierzą przejścia:  
	$$  
	P = \begin{bmatrix}  
	0.7 & 0.2 & 0.1 \\  
	0.3 & 0.5 & 0.2 \\  
	0.1 & 0.3 & 0.6 \\ 
	\end{bmatrix}  
	$$
	
	- $P_{12} = 0.2$ oznacza prawdopodobieństwo przejścia z stanu $1$ do stanu $2$.
	
	### 2.2. Rozkład stacjonarny
	
	Rozkład stacjonarny $\pi$ to wektor prawdopodobieństw $\pi = [\pi_1, \pi_2, \ldots]$, taki że:  
	$\pi P = \pi, \quad \sum_i \pi_i = 1, \quad \pi_i \geq 0.$  
	Oznacza to, że jeśli rozkład początkowy jest stacjonarny, to rozkład prawdopodobieństw stanów nie zmienia się w czasie.
	
	**Metoda obliczania**:
	
	1. Rozwiąż układ równań: $\pi P = \pi$, czyli $(\pi (P - I) = 0)$.
	2. Dodaj warunek normalizacji: $\sum_i \pi_i = 1$.
	3. Rozwiąż układ liniowy, np. metodą Gaussa.
	
	**Przykład**:  
	Dla macierzy $P$ podanej powyżej, rozwiązujemy:
	
	- $\pi P = \pi$ prowadzi do układu równań liniowych.
	- Po rozwiązaniu (z warunkiem $\sum \pi_i = 1$): $\pi \approx [0.357, 0.357, 0.286]$.
	
	**Warunki istnienia**:
	
	- Łańcuch musi być **nieodwracalny** (istnieje tylko jeden rozkład stacjonarny).
	- Łańcuch musi być **ergodyczny** (wszystkie stany są osiągalne i powracające), aby rozkład stacjonarny był osiągalny w granicy.
	
	### 2.3. Własności łańcuchów Markowa
	
	- **Klasyfikacja stanów**:
	    - **Powracające**: Prawdopodobieństwo powrotu do stanu jest równe 1.
	    - **Przejściowe**: Prawdopodobieństwo powrotu < 1.
	    - **Okresowe**: Stan ma okres $d > 1$, jeśli powroty są możliwe tylko w wielokrotnościach $d$.
	- **Zbieżność do rozkładu stacjonarnego**: Jeśli łańcuch jest nieodwracalny i aperiodyczny, rozkład stanów zbiega do $\pi$ dla $n \to \infty$.
	
	### 2.4. Zastosowania w informatyce
	
	- **Algorytmy losowe**: Algorytm PageRank (Google) opiera się na łańcuchu Markowa modelującym przechodzenie między stronami internetowymi.
	- **Sieci kolejkowe**: Modelowanie wydajności systemów komputerowych.
	- **Uczenie maszynowe**: Modelowanie sekwencji w modelach ukrytych Markowa (HMM).
	
	## 3. Zastosowania w informatyce
	
	- **Zmienne losowe**:
	    - Dyskretne: Analiza algorytmów losowych, modelowanie błędów w transmisji danych.
	    - Ciągłe: Symulacje Monte Carlo, analiza sygnałów, estymacja parametrów w ML.
	- **Łańcuchy Markowa**:
	    - Modelowanie systemów dynamicznych (np. protokoły sieciowe).
	    - Optymalizacja w algorytmach przeszukiwania grafów.
	    - Analiza niezawodności systemów (czas do awarii).

#### 5. Rachunek prawdopodobieństwa: testy statystyczne, test z, test t-Studenta, test chi-kwadrat. Wzór Bayesa i jego interpretacja.
1. Testy statystyczne
	
	Testy statystyczne służą do weryfikacji hipotez statystycznych na podstawie danych próbnych. Hipoteza zerowa ($H_0$) zakłada brak efektu lub różnicy, a hipoteza alternatywna ($H_1$) wskazuje na istnienie efektu. Testy opierają się na statystykach testowych i poziomie istotności $\alpha$ (np. 0.05), który określa próg odrzucenia $H_0$.
	1. Test z (test normalny)
		
		Test z jest stosowany do weryfikacji hipotez dotyczących średniej populacji, gdy wariancja populacji ($\sigma^2$) jest znana, a próba jest duża ($n \geq 30$) lub dane mają rozkład normalny.
		
		**Statystyka testowa**:  
		Dla średniej próbnej $\bar{x}$, średniej populacyjnej $\mu_0$ (z $H_0$), i wariancji populacyjnej $\sigma^2$:  
		$z = \frac{\bar{x} - \mu_0}{\sigma / \sqrt{n}},$  
		gdzie $n$ to rozmiar próby. Statystyka $z$ ma rozkład normalny standardowy $N(0,1)$.
		
		**Procedura**:
		
		1. Sformułuj hipotezy:
		    - $H_0$: $\mu = \mu_0$,
		    - $H_1$: $\mu \neq \mu_0$ (dwustronny) lub $\mu > \mu_0$ / $\mu < \mu_0$ (jednostronny).
		2. Oblicz statystykę $z$.
		3. Porównaj $z$ z wartością krytyczną $z_{\alpha/2}$ (dla testu dwustronnego) lub oblicz p-wartość:  
		    $p = P(Z > |z|) \cdot 2$ (dwustronny) lub $P(Z > z)$ (jednostronny).
		4. Odrzuć $H_0$, jeśli $p < \alpha$ lub $|z| > z_{\alpha/2}$.
		
		**Przykład**:  
		Testujemy, czy średni czas odpowiedzi serwera wynosi $\mu_0 = 100$ ms, przy $\sigma = 15$ ms, na podstawie próby $n=36$ z $\bar{x} = 104$ ms, $\alpha = 0.05$.
		
		- Statystyka: $z = \frac{104 - 100}{15 / \sqrt{36}} = \frac{4}{2.5} = 1.6$.
		- Dla $\alpha = 0.05$, wartość krytyczna $z_{0.025} \approx 1.96$ (dwustronny).
		- Ponieważ $|1.6| < 1.96$, nie odrzucamy $H_0$. p-wartość: $p = 2 \cdot P(Z > 1.6) \approx 0.109 > 0.05$.
		
		**Zastosowanie w informatyce**: Analiza wydajności systemów (np. czas odpowiedzi serwera), testowanie algorytmów.
	2. Test t-Studenta
		
		Test t-Studenta stosuje się, gdy wariancja populacji jest nieznana, a próba jest mała ($n < 30$) lub dane mają rozkład normalny.
		
		**Statystyka testowa**:  
		Dla średniej próbnej $\bar{x}$, wariancji próbnej $s^2$ i średniej populacyjnej $\mu_0$:  
		$t = \frac{\bar{x} - \mu_0}{s / \sqrt{n}},$  
		gdzie $s$ to odchylenie standardowe próby, a statystyka $t$ ma rozkład t-Studenta z $n-1$ stopniami swobody.
		
		**Procedura**:
		
		1. Sformułuj hipotezy: $H_0$: $\mu = \mu_0$, $H_1$: $\mu \neq \mu_0$ (lub jednostronny).
		2. Oblicz $t$.
		3. Porównaj $t$ z wartością krytyczną $t_{\alpha/2, n-1}$ lub oblicz p-wartość.
		4. Odrzuć $H_0$, jeśli $p < \alpha$ lub $|t| > t_{\alpha/2, n-1}$.
		
		**Przykład**:  
		Testujemy, czy średni czas obliczeń algorytmu wynosi $\mu_0 = 50$ ms, na podstawie próby $n=10$, $\bar{x} = 55$ ms, $s = 8$ ms, $\alpha = 0.05$.
		
		- Statystyka: $t = \frac{55 - 50}{8 / \sqrt{10}} \approx 1.98$.
		- Dla $n-1 = 9$ stopni swobody, $t_{0.025, 9} \approx 2.262$.
		- Ponieważ $|1.98| < 2.262$, nie odrzucamy $H_0$. p-wartość: $p \approx 0.08 > 0.05$.
		
		**Zastosowanie w informatyce**: Testowanie wydajności algorytmów na małych próbkach, analiza danych eksperymentalnych.
	3. Test chi-kwadrat
		
		Test chi-kwadrat stosuje się do analizy zgodności rozkładu danych z oczekiwanym rozkładem lub do testowania niezależności zmiennych kategorycznych.
		
		**Statystyka testowa**:  
		Dla obserwowanych częstości $O_i$ i oczekiwanych $E_i$:  
		$\chi^2 = \sum_{i} \frac{(O_i - E_i)^2}{E_i},$  
		gdzie $\chi^2$ ma rozkład chi-kwadrat z $k-1$ stopniami swobody (dla testu zgodności) lub $(r-1)(c-1)$ (dla testu niezależności, gdzie $r$ i $c$ to liczba wierszy i kolumn w tablicy kontyngencji).
		
		**Procedura**:
		
		1. Sformułuj hipotezy:
		    - Zgodność: $H_0$: Dane mają założony rozkład, $H_1$: Rozkład różni się.
		    - Niezależność: $H_0$: Zmienne są niezależne, $H_1$: Zmienne są zależne.
		2. Oblicz $\chi^2$.
		3. Porównaj z wartością krytyczną $\chi^2_{\alpha, df}$ lub oblicz p-wartość: $p = P(\chi^2 > \chi^2_{\text{obliczone}})$.
		4. Odrzuć $H_0$, jeśli $p < \alpha$ lub $\chi^2 > \chi^2_{\alpha, df}$.
		
		**Przykład (test zgodności)**:  
		Testujemy, czy rozkład błędów w systemie (kategorie: A, B, C) jest jednostajny. Obserwowane częstości: $O = [30, 40, 50]$, oczekiwane: $E = [40, 40, 40]$, $n=120$, $\alpha = 0.05$.
		
		- Statystyka: $\chi^2 = \frac{(30-40)^2}{40} + \frac{(40-40)^2}{40} + \frac{(50-40)^2}{40} = 2.5 + 0 + 2.5 = 5$.
		- Stopnie swobody: $k-1 = 3-1 = 2$, $\chi^2_{0.05, 2} \approx 5.991$.
		- Ponieważ $5 < 5.991$, nie odrzucamy $H_0$. p-wartość: $p \approx 0.082 > 0.05$.
		
		**Zastosowanie w informatyce**: Analiza rozkładu błędów, testowanie niezależności cech w danych (np. w uczeniu maszynowym).
2. Wzór Bayesa i jego interpretacja
	
	Wzór Bayesa pozwala aktualizować prawdopodobieństwa w oparciu o nowe dane. Dla zdarzeń $A$ i $B$, gdzie $P(B) > 0$:  
	$P(A|B) = \frac{P(B|A) P(A)}{P(B)},$  
	gdzie:
	
	- $P(A|B)$: Prawdopodobieństwo warunkowe zdarzenia $A$ przy zaistnieniu $B$ (prawdopodobieństwo a posteriori).
	- $P(B|A)$: Prawdopodobieństwo warunkowe $B$ przy $A$ (likelihood).
	- $P(A)$: Prawdopodobieństwo a priori zdarzenia $A$.
	- $P(B)$: Prawdopodobieństwo $B$, często obliczane jako:  
	    $P(B) = \sum_i P(B|A_i) P(A_i),$  
	    gdzie $A_i$ to rozłączne zdarzenia pokrywające przestrzeń $\Omega$.
	
	 Interpretacja
	
	Wzór Bayesa opisuje, jak nowe informacje ($B$) zmieniają nasze początkowe przekonania ($P(A)$) o zdarzeniu $A$. Jest podstawą wnioskowania bayesowskiego, które łączy wiedzę a priori z danymi empirycznymi.
	
	**Przykład**:  
	Test na obecność błędu w oprogramowaniu ma czułość $P(\text{pozytywny}|\text{błąd}) = 0.95$ i specyficzność $P(\text{negatywny}|\text{brak błędu}) = 0.98$. Prawdopodobieństwo błędu to $P(\text{błąd}) = 0.01$. Jaka jest szansa błędu przy pozytywnym wyniku testu?
	
	- Dane:
	    - $P(\text{pozytywny}|\text{błąd}) = 0.95$,
	    - $P(\text{pozytywny}|\text{brak błędu}) = 1 - 0.98 = 0.02$,
	    - $P(\text{błąd}) = 0.01$, $P(\text{brak błędu}) = 0.99$.
	- Oblicz $P(\text{pozytywny})$:  
	    $P(\text{pozytywny}) = 0.95 \cdot 0.01 + 0.02 \cdot 0.99 = 0.0095 + 0.0198 = 0.0293$.
	- Wzór Bayesa:  
	    $P(\text{błąd}|\text{pozytywny}) = \frac{0.95 \cdot 0.01}{0.0293} \approx 0.324$.
	- Interpretacja: Przy pozytywnym wyniku testu szansa błędu wynosi ok. 32.4%.
	
	### 2.3. Zastosowania w informatyce
	
	- **Uczenie maszynowe**: Naiwne klasyfikatory bayesowskie (np. w filtrach spamu).
	- **Diagnostyka systemów**: Ocena niezawodności oprogramowania lub sprzętu.
	- **Optymalizacja**: Aktualizacja modeli w systemach rekomendacyjnych.
	
	## 3. Zastosowania w informatyce
	
	- **Testy statystyczne**:
	    - Test z: Analiza dużych zbiorów danych (np. wydajność sieci).
	    - Test t-Studenta: Weryfikacja hipotez w eksperymentach z algorytmami.
	    - Test chi-kwadrat: Analiza rozkładów błędów, feature selection w ML.
	- **Wzór Bayesa**: Modelowanie niepewności w systemach AI, analiza ryzyka w cyberbezpieczeństwie, przetwarzanie sygnałów.
 
 
#### 6. Algebra liniowa: ortogonalność wektorów w przestrzeni $R^N$ związki z liniową niezależznością. Metoda ortonormalizacji Grama-Schmidta
1. Ortogonalność wektorów w przestrzeni $\mathbb{R}^n$
	
	### 1.1. Definicje
	
	W przestrzeni euklidesowej $\mathbb{R}^n$ z iloczynem skalarnym zdefiniowanym jako:  
	$\langle \mathbf{u}, \mathbf{v} \rangle = u_1 v_1 + u_2 v_2 + \cdots + u_n v_n,$  
	dla wektorów $\mathbf{u} = [u_1, u_2, \ldots, u_n]^T$ i $\mathbf{v} = [v_1, v_2, \ldots, v_n]^T$, mówimy, że:
	
	- **Ortogonalność**: Dwa wektory $\mathbf{u}$ i $\mathbf{v}$ są ortogonalne, jeśli $\langle \mathbf{u}, \mathbf{v} \rangle = 0$.
	- **Ortonormalność**: Zbiór wektorów ${\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k}$ jest ortonormalny, jeśli:
	    - $\langle \mathbf{v}_i, \mathbf{v}_j \rangle = 0$ dla $i \neq j$ (ortogonalność),
	    - $\langle \mathbf{v}_i, \mathbf{v}_i \rangle = 1$ (norma wektora wynosi 1, czyli $||\mathbf{v}_i|| = \sqrt{\langle \mathbf{v}_i, \mathbf{v}_i \rangle} = 1$).
	- **Zbiór ortogonalny**: Zbiór wektorów, w którym każdy wektor jest ortogonalny do pozostałych, ale niekoniecznie mają normę 1.
	
	**Norma wektora**:  
	$||\mathbf{v}|| = \sqrt{\langle \mathbf{v}, \mathbf{v} \rangle} = \sqrt{v_1^2 + v_2^2 + \cdots + v_n^2}.$
	
	### 1.2. Własności
	
	- **Baza ortogonalna**: Jeśli zbiór wektorów ${\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_n}$ jest ortogonalny i rozpięty na $\mathbb{R}^n$, to stanowi bazę przestrzeni. Współrzędne dowolnego wektora $\mathbf{x}$ w tej bazie można wyznaczyć jako:  
	    $\mathbf{x} = \sum_{i=1}^n \frac{\langle \mathbf{x}, \mathbf{v}_i \rangle}{\langle \mathbf{v}_i, \mathbf{v}_i \rangle} \mathbf{v}_i.$
	- **Ortonormalna baza**: Jeśli baza jest dodatkowo ortonormalna, to współrzędne upraszczają się do:  
	    $\mathbf{x} = \sum_{i=1}^n \langle \mathbf{x}, \mathbf{v}_i \rangle \mathbf{v}_i.$
	
	### 1.3. Zastosowania
	
	- **Przetwarzanie sygnałów**: Ortogonalne bazy (np. w transformacie Fouriera) ułatwiają analizę sygnałów.
	- **Uczenie maszynowe**: Ortogonalność wektorów cech w PCA (analiza głównych składowych).
	- **Metody numeryczne**: Stabilność obliczeń w algorytmach wymagających baz ortogonalnych.

2. Związki z liniową niezależnością
	
	1. Liniowa niezależność
		Zbiór wektorów ${\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k}$ w $\mathbb{R}^n$ jest liniowo niezależny, jeśli jedynym rozwiązaniem równania:  
		$c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \cdots + c_k \mathbf{v}_k = \mathbf{0}$  
		jest $c_1 = c_2 = \cdots = c_k = 0$.
	
	2. Ortogonalność a liniowa niezależność
		- **Twierdzenie**: Zbiór niezerowych wektorów ortogonalnych jest liniowo niezależny.
		- **Dowód**:  
		    Rozważmy zbiór ortogonalny ${\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k}$. Załóżmy, że:  
		    $c_1 \mathbf{v}_1 + c_2 \mathbf{v}_2 + \cdots + c_k \mathbf{v}_k = \mathbf{0}.$  
		    Pomnóżmy obustronnie przez $\mathbf{v}_i$ (iloczyn skalarny):  
		    $\langle c_1 \mathbf{v}_1 + \cdots + c_k \mathbf{v}_k, \mathbf{v}_i \rangle = \langle \mathbf{0}, \mathbf{v}_i \rangle = 0.$  
		    Z ortogonalności: $\langle \mathbf{v}_j, \mathbf{v}_i \rangle = 0$ dla $j \neq i$, więc:  
		    $c_i \langle \mathbf{v}_i, \mathbf{v}_i \rangle = 0.$  
		    Ponieważ $\mathbf{v}_i \neq \mathbf{0}$, to $\langle \mathbf{v}_i, \mathbf{v}_i \rangle > 0$, zatem $c_i = 0$ dla każdego $i$. Stąd zbiór jest liniowo niezależny.
	
	3. Implikacje
		- Ortogonalność zapewnia liniową niezależność, co jest kluczowe dla konstrukcji baz przestrzeni wektorowych.
		- W przestrzeniach o wysokim wymiarze (np. w informatyce) ortogonalne wektory upraszczają obliczenia, np. w rozwiązywaniu układów równań liniowych.

3. Metoda ortonormalizacji Grama-Schmidta
	Metoda Grama-Schmidta przekształca zbiór liniowo niezależnych wektorów ${\mathbf{u}_1, \mathbf{u}_2, \ldots, \mathbf{u}_k}$ w przestrzeni $\mathbb{R}^n$ w zbiór ortonormalny ${\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k}$, który rozpięty jest na tej samej przestrzeni.
	
	1. Algorytm
		
		Dla zbioru ${\mathbf{u}_1, \mathbf{u}_2, \ldots, \mathbf{u}_k}$:
		
		1. Ustaw $\mathbf{v}_1 = \frac{\mathbf{u}_1}{||\mathbf{u}_1||}$ (normalizacja pierwszego wektora).
		2. Dla $i = 2, 3, \ldots, k$:
		    - Oblicz wektor ortogonalny do poprzednich:  
		        $\mathbf{w}_i = \mathbf{u}_i - \sum_{j=1}^{i-1} \langle \mathbf{u}_i, \mathbf{v}_j \rangle \mathbf{v}_j.$
		    - Normalizuj: $\mathbf{v}_i = \frac{\mathbf{w}_i}{||\mathbf{w}_i||}$.
		3. Wynikowy zbiór ${\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k}$ jest ortonormalny.
	2. Przykład
		
		Rozważmy wektory w $\mathbb{R}^3$:  
		$\mathbf{u}_1 = \begin{bmatrix} 1 \ 1 \ 0 \end{bmatrix}, \mathbf{u}_2 = \begin{bmatrix} 1 \ 0 \ 1 \end{bmatrix}.$
		
		- Krok 1: $\mathbf{v}_1 = \frac{\mathbf{u}_1}{||\mathbf{u}_1||} = \frac{\begin{bmatrix} 1 \ 1 \ 0 \end{bmatrix}}{\sqrt{1^2 + 1^2}} = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \ 1 \ 0 \end{bmatrix}$.
		- Krok 2: Oblicz $\mathbf{w}_2 = \mathbf{u}_2 - \langle \mathbf{u}_2, \mathbf{v}_1 \rangle \mathbf{v}_1$:
		    - $\langle \mathbf{u}_2, \mathbf{v}_1 \rangle = \begin{bmatrix} 1 \ 0 \ 1 \end{bmatrix} \cdot \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \ 1 \ 0 \end{bmatrix} = \frac{1}{\sqrt{2}} (1 \cdot 1 + 0 \cdot 1 + 1 \cdot 0) = \frac{1}{\sqrt{2}}$.
		    - $\mathbf{w}_2 = \begin{bmatrix} 1 \ 0 \ 1 \end{bmatrix} - \frac{1}{\sqrt{2}} \cdot \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \ 1 \ 0 \end{bmatrix} = \begin{bmatrix} 1 \ 0 \ 1 \end{bmatrix} - \frac{1}{2} \begin{bmatrix} 1 \ 1 \ 0 \end{bmatrix} = \begin{bmatrix} 0.5 \ -0.5 \ 1 \end{bmatrix}$.
		    - Normalizuj: $||\mathbf{w}_2|| = \sqrt{0.5^2 + (-0.5)^2 + 1^2} = \sqrt{1.5}$, $\mathbf{v}_2 = \frac{\begin{bmatrix} 0.5 \ -0.5 \ 1 \end{bmatrix}}{\sqrt{1.5}} = \frac{1}{\sqrt{1.5}} \begin{bmatrix} 0.5 \ -0.5 \ 1 \end{bmatrix}$.
		- Wynik: ${\mathbf{v}_1, \mathbf{v}_2}$ jest ortonormalny.
	3. Własności
		
		- **Zalety**: Tworzy ortonormalną bazę, która upraszcza obliczenia (np. projekcje wektorów).
		- **Wady**: Wrażliwość na błędy numeryczne w obliczeniach komputerowych (np. utrata ortogonalności przy dużych $n$).
		- **Modyfikacje**: Stabilniejsza wersja (modyfikowany proces Grama-Schmidta) używa iteracyjnej projekcji w inny sposób, aby zminimalizować błędy zaokrągleń.
	4. Zastosowania w informatyce
		
		- **Rozkład QR**: Metoda Grama-Schmidta jest podstawą algorytmu rozkładu QR, używanego w rozwiązywaniu układów liniowych.
		- **Przetwarzanie sygnałów**: Ortogonalne bazy w kompresji danych (np. JPEG).
		- **Uczenie maszynowe**: PCA i SVD opierają się na ortogonalnych wektorach własnych.

4. Zastosowania w informatyce
	
	- **Ortogonalność**: Upraszcza obliczenia w algorytmach numerycznych, np. w metodzie najmniejszych kwadratów.
	- **Liniowa niezależność**: Kluczowa w analizie przestrzeni wektorowych w algorytmach grafowych i ML.
	- **Metoda Grama-Schmidta**: Używana w implementacji algorytmów wymagających ortogonalnych baz, np. w analizie danych wielowymiarowych.


#### 7. Podstawy teorii liczb: rozszerzony algorytm Euklidesa. Twierdzenia Eulera i Fermata; funkcja Eulera.

1. Rozszerzony algorytm Euklidesa
	
	1. Algorytm Euklidesa
		
		Algorytm Euklidesa służy do obliczania największego wspólnego dzielnika (NWD) dwóch liczb całkowitych $a$ i $b$. Opiera się na obserwacji, że:  
		$\text{NWD}(a, b) = \text{NWD}(b, a \mod b).$
		
		**Algorytm**:
		
		1. Weź dwie liczby całkowite $a$ i $b$ ($a \geq b \geq 0$).
		2. Dopóki $b \neq 0$:
		    - Oblicz $r = a \mod b$.
		    - Ustaw $a = b$, $b = r$.
		3. Wynik: $\text{NWD}(a, b) = a$.
		
		**Przykład**:  
		Obliczmy $\text{NWD}(48, 18)$:
		
		- $48 \div 18 = 2$ reszty $12$ → $\text{NWD}(48, 18) = \text{NWD}(18, 12)$.
		- $18 \div 12 = 1$ reszty $6$ → $\text{NWD}(18, 12) = \text{NWD}(12, 6)$.
		- $12 \div 6 = 2$ reszty $0$ → $\text{NWD}(12, 6) = 6$.  
		    Wynik: $\text{NWD}(48, 18) = 6$.
	
	2. Rozszerzony algorytm Euklidesa
		
		Rozszerzony algorytm Euklidesa, poza NWD, znajduje współczynniki $x$ i $y$ w tożsamości Bézouta:  
		$ax + by = \text{NWD}(a, b).$
		
		**Algorytm**:
		
		1. Inicjalizuj: $x_0 = 1$, $x_1 = 0$, $y_0 = 0$, $y_1 = 1$, $r_0 = a$, $r_1 = b$.
		2. Dopóki $r_1 \neq 0$:
		    - Oblicz iloraz $q = \lfloor r_0 / r_1 \rfloor$ i resztę $r_2 = r_0 - q r_1$.
		    - Oblicz nowe współczynniki: $x_2 = x_0 - q x_1$, $y_2 = y_0 - q y_1$.
		    - Aktualizuj: $r_0 = r_1$, $r_1 = r_2$, $x_0 = x_1$, $x_1 = x_2$, $y_0 = y_1$, $y_1 = y_2$.
		3. Wynik: $\text{NWD}(a, b) = r_0$, a tożsamość Bézouta to $ax_0 + by_0 = r_0$.
		
		**Przykład**:  
		Dla $a = 48$, $b = 18$:
		
		- Inicjalizacja: $r_0 = 48$, $r_1 = 18$, $x_0 = 1$, $x_1 = 0$, $y_0 = 0$, $y_1 = 1$.
		- Krok 1: $q = \lfloor 48/18 \rfloor = 2$, $r_2 = 48 - 2 \cdot 18 = 12$, $x_2 = 1 - 2 \cdot 0 = 1$, $y_2 = 0 - 2 \cdot 1 = -2$.
		- Krok 2: $r_0 = 18$, $r_1 = 12$, $x_0 = 0$, $x_1 = 1$, $y_0 = 1$, $y_1 = -2$. Oblicz: $q = \lfloor 18/12 \rfloor = 1$, $r_2 = 18 - 1 \cdot 12 = 6$, $x_2 = 0 - 1 \cdot 1 = -1$, $y_2 = 1 - 1 \cdot (-2) = 3$.
		- Krok 3: $r_0 = 12$, $r_1 = 6$, $x_0 = 1$, $x_1 = -1$, $y_0 = -2$, $y_1 = 3$. Oblicz: $q = \lfloor 12/6 \rfloor = 2$, $r_2 = 12 - 2 \cdot 6 = 0$, $x_2 = 1 - 2 \cdot (-1) = 3$, $y_2 = -2 - 2 \cdot 3 = -8$.
		- Wynik: $\text{NWD}(48, 18) = 6$, tożsamość Bézouta: $48 \cdot 3 + 18 \cdot (-8) = 144 - 144 = 6$.
		
		**Zastosowanie w informatyce**:
		
		- Kryptografia: Obliczanie odwrotności modularnej w RSA (jeśli $\text{NWD}(a, m) = 1$, to $x$ z tożsamości Bézouta to odwrotność $a$ modulo $m$).
		- Algorytmy: Rozwiązywanie równań diofantycznych, uproszczenie ułamków.

 2. Funkcja Eulera
	
	Funkcja Eulera $\phi(n)$ dla liczby naturalnej $n$ określa liczbę dodatnich liczb całkowitych mniejszych lub równych $n$, które są z $n$ wzajemnie pierwsze, czyli $\text{NWD}(k, n) = 1$ dla $1 \leq k \leq n$.
	
	**Wzór**:  
	Dla $n$ o rozkładzie na czynniki pierwsze $n = p_1^{k_1} p_2^{k_2} \cdots p_m^{k_m}$:  
	$\phi(n) = n \prod_{i=1}^m \left(1 - \frac{1}{p_i}\right),$  
	gdzie $p_i$ to różne czynniki pierwsze.
	
	**Przykład**:  
	Obliczmy $\phi(12)$:
	
	- Rozkład: $12 = 2^2 \cdot 3^1$.
	- $\phi(12) = 12 \cdot \left(1 - \frac{1}{2}\right) \left(1 - \frac{1}{3}\right) = 12 \cdot \frac{1}{2} \cdot \frac{2}{3} = 4$.
	- Sprawdzenie: Liczby $1, 5, 7, 11$ są wzajemnie pierwsze z $12$ ($\text{NWD}(k, 12) = 1$), czyli $\phi(12) = 4$.
	
	**Własności**:
	
	- Jeśli $n$ jest pierwsza, to $\phi(n) = n - 1$.
	- Jeśli $\text{NWD}(m, n) = 1$, to $\phi(mn) = \phi(m) \phi(n)$.
	
	**Zastosowanie w informatyce**:
	
	- Kryptografia: Kluczowa w algorytmie RSA, gdzie $\phi(n)$ określa liczbę elementów w grupie $\mathbb{Z}_n^*$.
	- Analiza algorytmów: Ocena złożoności algorytmów modularnych.

3. Twierdzenia Eulera i Fermata
	
	1. Twierdzenie Eulera
		
		**Twierdzenie**: Jeśli $a$ i $n$ są wzajemnie pierwsze ($\text{NWD}(a, n) = 1$), to:  
		$a^{\phi(n)} \equiv 1 \pmod{n}.$
		
		**Dowód (zarys)**:
		
		- Grupa $\mathbb{Z}_n^*$ (liczb od $1$ do $n$ wzajemnie pierwszych z $n$) ma $\phi(n)$ elementów.
		- Z twierdzenia Lagrange’a dla grup: dla elementu $a \in \mathbb{Z}_n^*$, rząd $a$ dzieli rząd grupy $\phi(n)$, czyli $a^{\phi(n)} = 1$ w grupie, co odpowiada $a^{\phi(n)} \equiv 1 \pmod{n}$.
		
		**Przykład**:  
		Dla $a = 7$, $n = 12$, $\text{NWD}(7, 12) = 1$, $\phi(12) = 4$:  
		$7^4 = 2401$, $2401 \div 12 = 200$ reszty $1$, czyli $7^4 \equiv 1 \pmod{12}$.
	
	2. Twierdzenie Fermata (Małe twierdzenie Fermata)
		**Twierdzenie**: Jeśli $p$ jest liczbą pierwszą i $a$ nie jest podzielne przez $p$, to:  
		$a^{p-1} \equiv 1 \pmod{p}.$
		
		**Uwaga**: Jest to przypadek szczególny twierdzenia Eulera, ponieważ dla liczby pierwszej $p$, $\phi(p) = p-1$.
		
		**Przykład**:  
		Dla $a = 3$, $p = 5$:  
		$3^{5-1} = 3^4 = 81$, $81 \div 5 = 16$ reszty $1$, czyli $3^4 \equiv 1 \pmod{5}$.
	
	3. Zastosowania w informatyce
		- **Kryptografia RSA**: Twierdzenie Eulera jest podstawą obliczania kluczy prywatnych i publicznych. Dla $n = pq$ (iloczyn dwóch liczb pierwszych), $\phi(n) = (p-1)(q-1)$, a twierdzenie Eulera zapewnia, że $m^{\phi(n)} \equiv 1 \pmod{n}$ dla $m$ wzajemnie pierwszego z $n$.
		- **Testy pierwszosci**: Twierdzenie Fermata jest używane w probabilistycznych testach pierwszosci (np. test Fermata).
		- **Algorytmy modularne**: Upraszczanie potęg w obliczeniach modularnych (np. $a^k \mod n$).

4. Zastosowania w informatyce
	- **Rozszerzony algorytm Euklidesa**: Obliczanie odwrotności modularnych w kryptografii (RSA, Diffie-Hellman), rozwiązywanie równań modularnych.
	- **Funkcja Eulera**: Kluczowa w projektowaniu systemów kryptograficznych i analizie algorytmów.
	- **Twierdzenia Eulera i Fermata**: Podstawowe w kryptografii asymetrycznej, testowaniu liczb pierwszych i optymalizacji obliczeń modularnych.

#### 8. Matematyka dyskretna: liczby Stirlinga I i II rodzaju i ich interpretacja; konfiguracje i t-konfiguracje kombinatoryczne. Rozwiązywanie równań rekurencyjnych przy użyciu funkcji tworzących (generujących).

1. Liczby Stirlinga I i II rodzaju
    
    1. Liczby Stirlinga I rodzaju
        
        Liczby Stirlinga I rodzaju (oznaczane $s(n,k)$ lub $\left[\begin{array}{c} n \ k \end{array}\right]$) określają liczbę permutacji $n$-elementowego zbioru, które mają dokładnie $k$ cykli w ich rozkładzie cyklowym. Są to liczby ze znakiem, ponieważ uwzględniają parzystość permutacji.
        
        **Definicja**:  
        Liczba $s(n,k)$ to liczba permutacji ${1, 2, \ldots, n}$ z dokładnie $k$ rozłącznymi cyklami.  
        Wzór rekurencyjny:  
        $s(n,k) = s(n-1, k-1) + (n-1) s(n-1, k),$  
        z warunkami brzegowymi:
        
        - $s(n,0) = 0$ dla $n > 0$,
        - $s(0,0) = 1$,
        - $s(n,k) = 0$ dla $k > n$ lub $k < 0$.
        
        **Przykład**:  
        Obliczmy $s(4,2)$:
        
        - Z rekurencji: $s(4,2) = s(3,1) + 3 s(3,2)$.
        - Obliczmy $s(3,1)$: $s(3,1) = s(2,0) + 2 s(2,1) = 0 + 2 \cdot 1 = 2$.
        - Obliczmy $s(3,2)$: $s(3,2) = s(2,1) + 2 s(2,2) = 1 + 2 \cdot 1 = 3$.
        - Zatem: $s(4,2) = 2 + 3 \cdot 3 = 11$.  
            Wynik: Liczba permutacji 4-elementowych z 2 cyklami wynosi 11.
        
        **Interpretacja**:
        
        - Permutacje z $k$ cyklami (np. w grafach skierowanych lub analizie permutacji).
        - Zastosowanie w analizie algorytmów losowych permutacji.
    2. Liczby Stirlinga II rodzaju
        
        Liczby Stirlinga II rodzaju (oznaczane $S(n,k)$ lub $$\binom{n}{k}$$ określają liczbę sposobów podzielenia $n$-elementowego zbioru na $k$ niepustych, nieoznaczonych podzbiorów.
        
        **Definicja**:  
        $S(n,k)$ to liczba partycji zbioru ${1, 2, \ldots, n}$ na $k$ niepustych podzbiorów.  
        Wzór rekurencyjny:  
        $S(n,k) = S(n-1, k-1) + k S(n-1, k),$  
        z warunkami brzegowymi:
        
        - $S(n,0) = 0$ dla $n > 0$,
        - $S(0,0) = 1$,
        - $S(n,k) = 0$ dla $k > n$ lub $k < 0$.
        
        **Przykład**:  
        Obliczmy $S(4,2)$:
        
        - Z rekurencji: $S(4,2) = S(3,1) + 2 S(3,2)$.
        - Obliczmy $S(3,1)$: $S(3,1) = S(2,0) + 1 \cdot S(2,1) = 0 + 1 \cdot 1 = 1$.
        - Obliczmy $S(3,2)$: $S(3,2) = S(2,1) + 2 S(2,2) = 1 + 2 \cdot 1 = 3$.
        - Zatem: $S(4,2) = 1 + 2 \cdot 3 = 7$.  
            Wynik: Liczba partycji 4-elementowego zbioru na 2 podzbiory wynosi 7 (np. ${{1,2}, {3,4}}$, ${{1,3}, {2,4}}$, itp.).
        
        **Interpretacja**:
        
        - Partycje zbiorów w analizie kombinatorycznej.
        - Zastosowanie w algorytmach grupowania i klasyfikacji danych.
        
        **Zastosowanie w informatyce**:
        
        - Liczby Stirlinga I: Analiza struktur cyklicznych w algorytmach losowych permutacji.
        - Liczby Stirlinga II: Grupowanie danych w uczeniu maszynowym, analiza złożoności algorytmów klastrowania.
2. Konfiguracje i t-konfiguracje kombinatoryczne
    
    Konfiguracje kombinatoryczne to struktury opisujące rozmieszczenie elementów w określonych schematach, często z ograniczeniami. t-konfiguracje to uogólnienie, które uwzględnia dodatkowe parametry, takie jak liczba elementów w każdej grupie.
    
    **Definicja**:
    
    - **Konfiguracja**: Rozmieszczenie $n$ elementów w $k$ grupach (np. podzbiory, permutacje, rozmieszczenia z powtórzeniami).
    - **t-konfiguracja**: Rozmieszczenie $n$ elementów na $k$ grup, gdzie każda grupa spełnia dodatkowe warunki (np. minimalna/maksymalna liczba elementów).  
        Przykłady:
    - Liczba sposobów rozmieszczenia $n$ różnych elementów w $k$ oznaczonych skrzynkach: $k^n$.
    - Liczba partycji $n$ elementów na $k$ niepustych podzbiorów: $S(n,k)$ (liczby Stirlinga II rodzaju).
    - t-konfiguracja może określać np. partycje, gdzie każda grupa ma co najmniej $t$ elementów.
    
    **Przykład**:  
    Obliczmy liczbę sposobów podzielenia 5 elementów na 2 niepuste, nieoznaczone podzbiory ($S(5,2)$):
    
    - Z rekurencji: $S(5,2) = S(4,1) + 2 S(4,2)$.
    - $S(4,1) = 1$, $S(4,2) = 7$ (z poprzedniego przykładu).
    - $S(5,2) = 1 + 2 \cdot 7 = 15$.  
        Jeśli wprowadzimy warunek t-konfiguracji, że każdy podzbiór ma co najmniej 2 elementy:
    - Możliwe partycje: ${{1,2,3}, {4,5}}$, ${{1,2,4}, {3,5}}$, itp. (obliczenia wymagają dodatkowej analizy).
    
    **Zastosowanie w informatyce**:
    
    - Projektowanie algorytmów klastrowania i partycjonowania danych.
    - Analiza struktur danych, np. w bazach danych lub systemach rozproszonych.
    - Modelowanie problemów optymalizacyjnych, np. alokacja zasobów.
3. Rozwiązywanie równań rekurencyjnych przy użyciu funkcji tworzących
    
    Funkcje tworzące (generujące) to narzędzia do rozwiązywania równań rekurencyjnych poprzez reprezentację ciągu ${a_n}$ w postaci szeregu potęgowego lub wykładniczego. Umożliwiają przekształcenie rekurencji w równania algebraiczne.
    
    1. Funkcje tworzące
        
        **Definicja**:  
        Dla ciągu ${a_n}$, funkcja tworząca to:
        
        - Zwykła: $G(x) = \sum_{n=0}^\infty a_n x^n$,
        - Wykładnicza: $F(x) = \sum_{n=0}^\infty a_n \frac{x^n}{n!}$.  
            Funkcje zwykłe są najczęściej używane w kombinatoryce, a wykładnicze w analizie permutacji.
        
        **Metoda rozwiązywania**:
        
        1. Zapisz rekurencję w postaci równania funkcyjnego dla $G(x)$.
        2. Rozwiąż równanie algebraiczne dla $G(x)$.
        3. Rozwiń $G(x)$ w szereg, aby uzyskać współczynniki $a_n$.
        
        **Przykład**:  
        Rozwiążmy rekurencję: $a_n = a_{n-1} + a_{n-2}$, $a_0 = 0$, $a_1 = 1$ (ciąg Fibonacciego).
        
        - Funkcja tworząca: $G(x) = \sum_{n=0}^\infty a_n x^n$.
        - Pomnóż rekurencję przez $x^n$ i zsumuj:  
            $\sum_{n=2}^\infty a_n x^n = \sum_{n=2}^\infty a_{n-1} x^n + \sum_{n=2}^\infty a_{n-2} x^n$.
        - Równanie funkcyjne: $G(x) - a_0 - a_1 x = x (G(x) - a_0) + x^2 G(x)$.
        - Podstaw $a_0 = 0$, $a_1 = 1$: $G(x) - x = x G(x) + x^2 G(x)$.
        - Rozwiąż: $G(x) (1 - x - x^2) = x$, czyli $G(x) = \frac{x}{1 - x - x^2}$.
        - Rozłóż na ułamki proste: $1 - x - x^2 = (1 - \phi x)(1 - \hat{\phi} x)$, gdzie $\phi = \frac{1 + \sqrt{5}}{2}$, $\hat{\phi} = \frac{1 - \sqrt{5}}{2}$.
        - $G(x) = \frac{x}{(1 - \phi x)(1 - \hat{\phi} x)} = \frac{A}{1 - \phi x} + \frac{B}{1 - \hat{\phi} x}$.
        - Rozwiązując: $A = \frac{1}{\sqrt{5}}$, $B = -\frac{1}{\sqrt{5}}$.
        - $G(x) = \frac{1}{\sqrt{5}} \left( \frac{1}{1 - \phi x} - \frac{1}{1 - \hat{\phi} x} \right)$.
        - Rozwiń szeregi: $a_n = \frac{\phi^n - \hat{\phi}^n}{\sqrt{5}}$ (wzór Bineta).
        
        **Zastosowanie w informatyce**:
        
        - Analiza złożoności algorytmów rekurencyjnych (np. algorytmy dziel i zwyciężaj).
        - Generowanie ciągów w problemach kombinatorycznych.
        - Modelowanie struktur danych, np. drzew binarnych.
    2. Zastosowania w informatyce
        
        - Rozwiązywanie rekurencji w analizie algorytmów (np. czas działania algorytmów rekurencyjnych).
        - Projektowanie struktur danych, takich jak drzewa lub grafy.
        - Kombinatoryka w analizie sieci i systemów rozproszonych.
4. Zastosowania w informatyce
    
    - Liczby Stirlinga: Analiza struktur danych i algorytmów klastrowania, modelowanie permutacji w systemach losowych.
    - Konfiguracje kombinatoryczne: Projektowanie algorytmów partycjonowania, optymalizacja zasobów w systemach komputerowych.
    - Funkcje tworzące: Analiza złożoności algorytmów, generowanie ciągów w problemach kombinatorycznych, projektowanie struktur danych.
#### 9. Podstawy teorii grafów: Cykl Hamiltona, obwód Eulera, liczba chromatyczna – definicje i twierdzenia; algorytm Forda-Fulkersona wyznaczania maksymalnego przepływu.

1. Cykl Hamiltona
    
    1. Definicja i twierdzenia
        
        Cykl Hamiltona w grafie $G = (V, E)$ to cykl, który przechodzi dokładnie raz przez każdy wierzchołek grafu i wraca do wierzchołka początkowego. Graf posiadający cykl Hamiltona nazywany jest grafem hamiltonowskim.
        
        **Definicja**:  
        Cykl Hamiltona to zamknięta ścieżka $(v_1, v_2, \ldots, v_n, v_1)$, gdzie każdy wierzchołek $v_i \in V$ pojawia się dokładnie raz (oprócz $v_1$, które pojawia się na początku i końcu).
        
        **Twierdzenia**:
        
        - Twierdzenie Diraca (1952): Jeśli graf prosty $G$ ma $n \geq 3$ wierzchołków i każdy wierzchołek ma stopień co najmniej $\frac{n}{2}$, to $G$ jest hamiltonowski.
        - Twierdzenie Ore (1960): Jeśli dla każdej pary niew sąsiadujących wierzchołków $u, v$ w grafie prostym $G$ o $n \geq 3$ wierzchołkach zachodzi $\deg(u) + \deg(v) \geq n$, to $G$ jest hamiltonowski.
        - Uwaga: Warunki te są wystarczające, ale nie konieczne. Problem znajdowania cyklu Hamiltona jest NP-zupełny.
        
        **Przykład**:  
        Rozważmy graf pełny $K_4$ z wierzchołkami ${1, 2, 3, 4}$.
        
        - Cykl Hamiltona: $(1, 2, 3, 4, 1)$.
        - Graf $K_4$ spełnia warunki Diraca, ponieważ każdy wierzchołek ma stopień $3 \geq \frac{4}{2} = 2$.
        
        **Zastosowanie w informatyce**:
        
        - Problem komiwojażera (optymalizacja tras).
        - Planowanie zadań w systemach rozproszonych.
        - Analiza sieci komunikacyjnych.
2. Obwód Eulera
    
    1. Definicja i twierdzenia
        
        Obwód Eulera w grafie $G = (V, E)$ to zamknięta ścieżka, która przechodzi dokładnie raz przez każdą krawędź grafu i wraca do wierzchołka początkowego. Graf posiadający obwód Eulera nazywany jest grafem eulerowskim.
        
        **Definicja**:  
        Obwód Eulera to zamknięta ścieżka $(e_1, e_2, \ldots, e_m)$, gdzie każda krawędź $e_i \in E$ pojawia się dokładnie raz. Ścieżka Eulera to otwarta ścieżka obejmująca wszystkie krawędzie.
        
        **Twierdzenia**:
        
        - Twierdzenie Eulera (1736): Graf spójny $G$ ma obwód Eulera wtedy i tylko wtedy, gdy każdy wierzchołek ma parzysty stopień.
        - Graf spójny $G$ ma ścieżkę Eulera (niebędącą obwodem), jeśli dokładnie dwa wierzchołki mają nieparzysty stopień.
        - Algorytm znajdowania obwodu Eulera (np. algorytm Fleury’ego) jest efektywny (czas liniowy względem liczby krawędzi).
        
        **Przykład**:  
        Rozważmy graf $K_3$ (trójkąt) z wierzchołkami ${1, 2, 3}$.
        
        - Każdy wierzchołek ma stopień 2 (parzysty).
        - Obwód Eulera: $(1, 2, 3, 1)$.
        - W grafie $K_4$ z jednym usuniętym wierzchołkiem (np. tworzącym ścieżkę z dwoma wierzchołkami o nieparzystym stopniu) istnieje ścieżka Eulera, ale nie obwód.
        
        **Zastosowanie w informatyce**:
        
        - Routing w sieciach komputerowych.
        - Algorytmy dekodowania w kodowaniu DNA.
        - Optymalizacja w problemach transportowych.
3. Liczba chromatyczna
    
    1. Definicja i twierdzenia
        
        Liczba chromatyczna grafu $G$, oznaczana $\chi(G)$, to najmniejsza liczba kolorów potrzebna do pokolorowania wierzchołków grafu tak, aby żadne dwa sąsiednie wierzchołki nie miały tego samego koloru.
        
        **Definicja**:  
        Kolorowanie wierzchołków grafu $G = (V, E)$ to funkcja $c: V \to {1, 2, \ldots, k}$, taka że dla każdej krawędzi $(u, v) \in E$, $c(u) \neq c(v)$. Liczba chromatyczna $\chi(G)$ to minimalne $k$.
        
        **Twierdzenia**:
        
        - Twierdzenie Brooksa (1941): Dla grafu prostego spójnego $G$, który nie jest grafem pełnym ani cyklem nieparzystym, $\chi(G) \leq \Delta(G)$, gdzie $\Delta(G)$ to maksymalny stopień wierzchołka.
        - Twierdzenie o pięciu kolorach: Każdy graf planarny ma $\chi(G) \leq 5$.
        - Twierdzenie o czterech kolorach: Każdy graf planarny ma $\chi(G) \leq 4$ (udowodnione komputerowo w 1976).
        - Problem kolorowania grafu jest NP-zupełny dla ogólnych grafów.
        
        **Przykład**:  
        Rozważmy graf cyklu $C_4$ (czworokąt).
        
        - Pokolorowanie: Wierzchołki ${1, 3}$ kolor 1, wierzchołki ${2, 4}$ kolor 2.
        - Liczba chromatyczna: $\chi(C_4) = 2$, ponieważ sąsiednie wierzchołki wymagają różnych kolorów, a dwa kolory wystarczą.
        
        **Zastosowanie w informatyce**:
        
        - Przydział zasobów (np. alokacja rejestrów w kompilatorach).
        - Planowanie harmonogramów (np. unikanie konfliktów w harmonogramach zadań).
        - Alokacja częstotliwości w sieciach bezprzewodowych.
4. Algorytm Forda-Fulkersona wyznaczania maksymalnego przepływu
    
    1. Definicja i algorytm
        
        Algorytm Forda-Fulkersona służy do obliczania maksymalnego przepływu w sieci przepływowej, czyli największej możliwej wartości przepływu od źródła do ujścia w grafie skierowanym z wagami krawędzi (pojemnościami).
        
        **Definicja**:  
        Sieć przepływowa to graf skierowany $G = (V, E)$ z wyznaczonym źródłem $s$, ujściem $t$ i pojemnościami krawędzi $c(u,v) \geq 0$. Przepływ $f(u,v)$ na krawędzi $(u,v)$ spełnia:
        
        - Ograniczenie pojemności: $0 \leq f(u,v) \leq c(u,v)$,
        - Zachowanie przepływu: Dla każdego wierzchołka $v \neq s, t$, suma przepływów wchodzących równa się sumie przepływów wychodzących.  
            Maksymalny przepływ to największa wartość $\sum_{v} f(s,v)$ (przepływ wychodzący ze źródła).
        
        **Algorytm Forda-Fulkersona**:
        
        1. Inicjalizuj przepływ $f(u,v) = 0$ dla wszystkich krawędzi.
        2. Dopóki istnieje ścieżka powiększająca (ścieżka od $s$ do $t$ w grafie resztkowym $G_f$):
            - Znajdź ścieżkę powiększającą (np. za pomocą BFS lub DFS).
            - Oblicz minimalną resztkową pojemność $c_f$ na tej ścieżce.
            - Zaktualizuj przepływ: dla każdej krawędzi $(u,v)$ na ścieżce, $f(u,v) = f(u,v) + c_f$, a dla krawędzi odwrotnej $f(v,u) = f(v,u) - c_f$.
        3. Wynik: Wartość maksymalnego przepływu to suma przepływów wychodzących z $s$.
        
        **Graf resztkowy**:  
        Graf $G_f$ ma krawędzie $(u,v)$ z resztkową pojemnością $c_f(u,v) = c(u,v) - f(u,v)$ oraz krawędzie odwrotne $(v,u)$ z $c_f(v,u) = f(u,v)$ dla przepływu wstecznego.
        
        **Twierdzenie o maksymalnym przepływie i minimalnym przekroju**:  
        Wartość maksymalnego przepływu równa się wartości minimalnego przekroju $(S, T)$, gdzie $S$ zawiera $s$, a $T$ zawiera $t$.
        
        **Przykład**:  
        Rozważmy sieć z wierzchołkami ${s, a, b, t}$, krawędziami i pojemnościami: $(s,a: 3)$, $(s,b: 2)$, $(a,b: 1)$, $(a,t: 2)$, $(b,t: 3)$.
        
        - Inicjalny przepływ: $f = 0$.
        - Ścieżka powiększająca: $s \to a \to t$, $c_f = \min(3, 2) = 2$. Zaktualizuj: $f(s,a) = 2$, $f(a,t) = 2$.
        - Nowy graf resztkowy: $(s,a: 1)$, $(s,b: 2)$, $(a,b: 1)$, $(b,t: 3)$.
        - Ścieżka: $s \to b \to t$, $c_f = \min(2, 3) = 2$. Zaktualizuj: $f(s,b) = 2$, $f(b,t) = 2$.
        - Brak dalszych ścieżek powiększających. Maksymalny przepływ: $2 + 2 = 4$.
        
        **Zastosowanie w informatyce**:
        
        - Optymalizacja przepływu w sieciach komputerowych (np. routing danych).
        - Problemy parowania (np. parowanie dwudzielne).
        - Planowanie i alokacja zasobów w systemach rozproszonych.
    2. Zastosowania w informatyce
        
        - Modelowanie przepływu danych w sieciach telekomunikacyjnych.
        - Algorytmy parowania i przypisania zadań.
        - Analiza przepustowości w systemach rozproszonych.
5. Zastosowania w informatyce
    
    - Cykl Hamiltona: Optymalizacja tras w sieciach, planowanie zadań, analiza grafów w systemach rozproszonych.
    - Obwód Eulera: Routing w sieciach, projektowanie obwodów drukowanych, analiza sekwencji w bioinformatyce.
    - Liczba chromatyczna: Przydział zasobów (np. rejestry w kompilatorach), harmonogramowanie, alokacja częstotliwości.
    - Algorytm Forda-Fulkersona: Optymalizacja przepływu w sieciach, parowanie w grafach, analiza systemów transportowych.
#### 10. Analiza matematyczna – ciągi liczbowe, funkcje jednej zmiennej: granica, ciągłość i pochodna funkcji; ekstrema lokalne.

1. Ciągi liczbowe
    
    1. Granica ciągu
        
        Granica ciągu liczbowego określa wartość, do której ciąg dąży, gdy indeks $n$ rośnie do nieskończoności.
        
        **Definicja**:  
        Ciąg ${a_n}$ ma granicę $L$, zapisywaną $\lim_{n \to \infty} a_n = L$, jeśli dla każdego $\epsilon > 0$ istnieje $N \in \mathbb{N}$, takie że dla każdego $n > N$ zachodzi $|a_n - L| < \epsilon$. Jeśli granica nie istnieje, ciąg jest rozbieżny.
        
        **Twierdzenia**:
        
        - Twierdzenie o jednoznaczności granicy: Jeśli ciąg ma granicę, to jest ona jednoznaczna.
        - Twierdzenie o ciągu ograniczonym monotonicznym: Każdy ciąg monotoniczny i ograniczony jest zbieżny.
        - Twierdzenie o kleszczach: Jeśli $a_n \leq b_n \leq c_n$ oraz $\lim_{n \to \infty} a_n = \lim_{n \to \infty} c_n = L$, to $\lim_{n \to \infty} b_n = L$.
        
        **Przykład**:  
        Obliczmy granicę ciągu $a_n = \frac{2n + 1}{n + 2}$.
        
        - Dzielimy licznik i mianownik przez $n$: $a_n = \frac{2 + \frac{1}{n}}{1 + \frac{2}{n}}$.
        - Gdy $n \to \infty$, $\frac{1}{n} \to 0$, $\frac{2}{n} \to 0$, więc $a_n \to \frac{2 + 0}{1 + 0} = 2$.  
            Wynik: $\lim_{n \to \infty} \frac{2n + 1}{n + 2} = 2$.
        
        **Zastosowanie w informatyce**:
        
        - Analiza zbieżności algorytmów iteracyjnych (np. w metodach numerycznych).
        - Ocena złożoności obliczeniowej (np. analiza granic w analizie asymptotycznej).
        - Modelowanie procesów w systemach dynamicznych.
2. Funkcje jednej zmiennej: granica i ciągłość
    
    1. Granica funkcji
        
        Granica funkcji opisuje zachowanie funkcji $f(x)$, gdy argument $x$ dąży do określonego punktu lub nieskończoności.
        
        **Definicja**:  
        Funkcja $f$ ma granicę $L$ w punkcie $c$, zapisywaną $\lim_{x \to c} f(x) = L$, jeśli dla każdego $\epsilon > 0$ istnieje $\delta > 0$, takie że dla każdego $x$ spełniającego $0 < |x - c| < \delta$, zachodzi $|f(x) - L| < \epsilon$.  
        Granica w nieskończoności: $\lim_{x \to \infty} f(x) = L$, jeśli dla każdego $\epsilon > 0$ istnieje $M > 0$, takie że dla $x > M$, $|f(x) - L| < \epsilon$.
        
        **Twierdzenia**:
        
        - Twierdzenie o zachowaniu znaku: Jeśli $\lim_{x \to c} f(x) = L > 0$, to istnieje okolica $c$, w której $f(x) > 0$.
        - Twierdzenie o kleszczach dla funkcji: Jeśli $g(x) \leq f(x) \leq h(x)$ w okolicy $c$ i $\lim_{x \to c} g(x) = \lim_{x \to c} h(x) = L$, to $\lim_{x \to c} f(x) = L$.
        
        **Przykład**:  
        Obliczmy $\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$.
        
        - Dla $x \neq 2$: $\frac{x^2 - 4}{x - 2} = \frac{(x - 2)(x + 2)}{x - 2} = x + 2$.
        - Zatem: $\lim_{x \to 2} (x + 2) = 2 + 2 = 4$.  
            Wynik: $\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = 4$.
        
        **Zastosowanie w informatyce**:
        
        - Analiza stabilności algorytmów numerycznych.
        - Modelowanie procesów ciągłych w systemach czasu rzeczywistego.
    2. Ciągłość funkcji
        
        Ciągłość funkcji oznacza, że małe zmiany argumentu powodują małe zmiany wartości funkcji.
        
        **Definicja**:  
        Funkcja $f$ jest ciągła w punkcie $c$, jeśli:
        
        1. $\lim_{x \to c} f(x)$ istnieje,
        2. $f(c)$ jest określone,
        3. $\lim_{x \to c} f(x) = f(c)$.  
            Funkcja jest ciągła na przedziale, jeśli jest ciągła w każdym jego punkcie.
        
        **Twierdzenia**:
        
        - Twierdzenie o osiąganiu wartości: Jeśli $f$ jest ciągła na $[a, b]$, to przyjmuje każdą wartość między $f(a)$ a $f(b)$.
        - Twierdzenie o wartościach ekstremalnych: Jeśli $f$ jest ciągła na $[a, b]$, to osiąga swoje minimum i maksimum na tym przedziale.
        
        **Przykład**:  
        Sprawdźmy ciągłość funkcji $f(x) = \frac{1}{x}$ w punkcie $x = 0$.
        
        - Funkcja nie jest określona w $x = 0$, więc nie jest ciągła w tym punkcie.
        - Dla $x \neq 0$, $f(x)$ jest ciągła, bo $\lim_{x \to c} \frac{1}{x} = \frac{1}{c}$ dla $c \neq 0$.
        
        **Zastosowanie w informatyce**:
        
        - Projektowanie algorytmów numerycznych (np. interpolacja).
        - Analiza stabilności systemów w przetwarzaniu sygnałów.
3. Pochodna funkcji
    
    1. Definicja i interpretacja
        
        Pochodna funkcji mierzy tempo zmiany funkcji w danym punkcie i jest podstawą analizy lokalnych własności funkcji.
        
        **Definicja**:  
        Pochodna funkcji $f$ w punkcie $x$ to:  
        $f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$,  
        o ile granica istnieje. Geometrycznie, $f'(x)$ to nachylenie stycznej do wykresu $f$ w punkcie $x$.
        
        **Twierdzenia**:
        
        - Twierdzenie o wartości średniej: Jeśli $f$ jest ciągła na $[a, b]$ i różniczkowalna na $(a, b)$, to istnieje $c \in (a, b)$, takie że $f'(c) = \frac{f(b) - f(a)}{b - a}$.
        - Twierdzenie Rolle’a: Jeśli $f$ jest ciągła na $[a, b]$, różniczkowalna na $(a, b)$ i $f(a) = f(b)$, to istnieje $c \in (a, b)$, takie że $f'(c) = 0$.
        
        **Przykład**:  
        Obliczmy pochodną funkcji $f(x) = x^3$.
        
        - $f'(x) = \lim_{h \to 0} \frac{(x+h)^3 - x^3}{h} = \lim_{h \to 0} \frac{x^3 + 3x^2h + 3xh^2 + h^3 - x^3}{h} = \lim_{h \to 0} (3x^2 + 3xh + h^2) = 3x^2$.  
            Wynik: $f'(x) = 3x^2$.
        
        **Zastosowanie w informatyce**:
        
        - Optymalizacja algorytmów (np. metoda gradientowa).
        - Analiza dynamiki systemów w symulacjach komputerowych.
        - Przetwarzanie sygnałów i obrazów (np. wykrywanie krawędzi).
    2. Zastosowania w informatyce
        
        - Optymalizacja funkcji kosztu w uczeniu maszynowym (np. gradient descent).
        - Modelowanie dynamiki w systemach czasu rzeczywistego.
        - Analiza numeryczna w algorytmach aproksymacji.
4. Ekstrema lokalne
    
    1. Definicja i twierdzenia
        
        Ekstrema lokalne to punkty, w których funkcja osiąga lokalne maksimum lub minimum.
        
        **Definicja**:  
        Funkcja $f$ ma lokalne maksimum (minimum) w punkcie $c$, jeśli istnieje okolica $c$, taka że $f(x) \leq f(c)$ ($f(x) \geq f(c)$) dla wszystkich $x$ w tej okolicy.
        
        - Warunek konieczny: Jeśli $f$ jest różniczkowalna w $c$ i $c$ jest ekstremum lokalnym, to $f'(c) = 0$ (punkt krytyczny).
        - Warunek wystarczający (test drugiej pochodnej): Jeśli $f'(c) = 0$ i $f''(c) > 0$, to $c$ jest lokalnym minimum; jeśli $f''(c) < 0$, to $c$ jest lokalnym maksimum.
        
        **Twierdzenia**:
        
        - Twierdzenie Fermata: Jeśli $f$ ma ekstremum lokalne w $c$ i jest różniczkowalna w $c$, to $f'(c) = 0$.
        - Test pierwszej pochodnej: Jeśli $f'(x)$ zmienia znak w punkcie krytycznym $c$, to $c$ jest ekstremum lokalnym (z dodatniego na ujemny: maksimum, z ujemnego na dodatni: minimum).
        
        **Przykład**:  
        Znajdźmy ekstrema lokalne funkcji $f(x) = x^3 - 3x$.
        
        - Pochodna: $f'(x) = 3x^2 - 3 = 3(x^2 - 1)$. Punkty krytyczne: $x = \pm 1$.
        - Druga pochodna: $f''(x) = 6x$.
        - Dla $x = 1$: $f''(1) = 6 > 0$ → lokalne minimum.
        - Dla $x = -1$: $f''(-1) = -6 < 0$ → lokalne maksimum.  
            Wynik: Lokalne minimum w $x = 1$, $f(1) = 1 - 3 = -2$; lokalne maksimum w $x = -1$, $f(-1) = -1 + 3 = 2$.
        
        **Zastosowanie w informatyce**:
        
        - Optymalizacja hiperparametrów w uczeniu maszynowym.
        - Analiza wydajności algorytmów (np. minimalizacja czasu obliczeń).
        - Projektowanie systemów sterowania i regulacji.
    2. Zastosowania w informatyce
        
        - Optymalizacja algorytmów w uczeniu maszynowym i sztucznej inteligencji.
        - Analiza krzywych w grafice komputerowej (np. splajny).
        - Modelowanie systemów dynamicznych w symulacjach.
5. Zastosowania w informatyce
    
    - Ciągi liczbowe: Analiza zbieżności algorytmów, modelowanie procesów iteracyjnych.
    - Granica i ciągłość: Stabilność algorytmów numerycznych, projektowanie systemów czasu rzeczywistego.
    - Pochodna: Optymalizacja algorytmów, przetwarzanie sygnałów, analiza dynamiki systemów.
    - Ekstrema lokalne: Optymalizacja funkcji kosztu, projektowanie algorytmów w grafice komputerowej i systemach sterowania.
#### 11. Analiza matematyczna – funkcje wielu zmiennych: pochodne cząstkowe, różniczkowalność, ekstrema lokalne.

1. Pochodne cząstkowe
    
    1. Definicja i interpretacja
        
        Pochodne cząstkowe funkcji wielu zmiennych mierzą tempo zmiany funkcji wzdłuż jednej zmiennej, przy założeniu, że pozostałe zmienne są stałe.
        
        **Definicja**:  
        Dla funkcji $f(x_1, x_2, \ldots, x_n)$ pochodna cząstkowa względem zmiennej $x_i$ w punkcie $(a_1, a_2, \ldots, a_n)$ jest określona jako:  
    $$
\frac{\partial f}{\partial x_i}(a_1, a_2, \ldots, a_n) = \lim_{h \to 0} \frac{f(a_1, \ldots, a_i + h, \ldots, a_n) - f(a_1, \ldots, a_n)}{h}
$$
        o ile granica istnieje. Geometrycznie, $\frac{\partial f}{\partial x_i}$ to nachylenie stycznej do wykresu $f$ w kierunku osi $x_i$.
        
        **Twierdzenia**:
        
        - Twierdzenie Schwarza: Jeśli funkcja $f$ ma ciągłe pochodne cząstkowe drugiego rzędu w okolicy punktu, to $\frac{\partial^2 f}{\partial x_i \partial x_j} = \frac{\partial^2 f}{\partial x_j \partial x_i}$.
        - Pochodne cząstkowe wyższych rzędów definiuje się przez iteracyjne różniczkowanie, np. $\frac{\partial^2 f}{\partial x_i \partial x_j}$.
        
        **Przykład**:  
        Obliczmy pochodne cząstkowe funkcji $f(x, y) = x^2 y + 3xy^2$.
        
        - Względem $x$: $\frac{\partial f}{\partial x} = 2xy + 3y^2$.
        - Względem $y$: $\frac{\partial f}{\partial y} = x^2 + 6xy$.
        - Druga pochodna: $\frac{\partial^2 f}{\partial x \partial y} = \frac{\partial}{\partial x} (x^2 + 6xy) = 2x + 6y$.  
            Wynik: $\frac{\partial f}{\partial x} = 2xy + 3y^2$, $\frac{\partial f}{\partial y} = x^2 + 6xy$, $\frac{\partial^2 f}{\partial x \partial y} = 2x + 6y$.
        
        **Zastosowanie w informatyce**:
        
        - Optymalizacja w uczeniu maszynowym (np. obliczanie gradientów w metodzie gradientowej).
        - Analiza numeryczna w modelowaniu fizycznym (np. równania różniczkowe cząstkowe).
        - Przetwarzanie obrazów (np. wykrywanie krawędzi w obrazie 2D).
2. Różniczkowalność
    
    1. Definicja i warunki
        
        Różniczkowalność funkcji wielu zmiennych to uogólnienie pojęcia pochodnej, uwzględniające zmiany we wszystkich kierunkach.
        
        **Definicja**:  
        Funkcja $f: \mathbb{R}^n \to \mathbb{R}$ jest różniczkowalna w punkcie $\mathbf{a} = (a_1, a_2, \ldots, a_n)$, jeśli istnieje wektor gradientu $\nabla f(\mathbf{a}) = \left( \frac{\partial f}{\partial x_1}, \ldots, \frac{\partial f}{\partial x_n} \right)$ oraz funkcja $r(\mathbf{h})$ taka, że:  
        [  
        f(\mathbf{a} + \mathbf{h}) = f(\mathbf{a}) + \nabla f(\mathbf{a}) \cdot \mathbf{h} + r(\mathbf{h}),  
        ]  
        gdzie $\lim_{\mathbf{h} \to \mathbf{0}} \frac{r(\mathbf{h})}{|\mathbf{h}|} = 0$. Gradient $\nabla f$ określa kierunek największego wzrostu funkcji.
        
        **Twierdzenia**:
        
        - Jeśli funkcja $f$ ma ciągłe pochodne cząstkowe w okolicy punktu $\mathbf{a}$, to jest różniczkowalna w $\mathbf{a}$.
        - Twierdzenie o aproksymacji liniowej: W pobliżu $\mathbf{a}$, funkcja $f$ jest aproksymowana przez płaszczyznę styczną: $f(\mathbf{x}) \approx f(\mathbf{a}) + \nabla f(\mathbf{a}) \cdot (\mathbf{x} - \mathbf{a})$.
        
        **Przykład**:  
        Sprawdźmy, czy funkcja $f(x, y) = x^2 + y^2$ jest różniczkowalna w $(1, 1)$.
        
        - Gradient: $\nabla f(x, y) = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right) = (2x, 2y)$, w $(1, 1)$: $\nabla f(1, 1) = (2, 2)$.
        - Pochodne cząstkowe $\frac{\partial f}{\partial x} = 2x$, $\frac{\partial f}{\partial y} = 2y$ są ciągłe, więc $f$ jest różniczkowalna w $(1, 1)$.
        - Aproksymacja liniowa: $f(x, y) \approx f(1, 1) + \nabla f(1, 1) \cdot (x-1, y-1) = 2 + 2(x-1) + 2(y-1) = 2x + 2y - 2$.  
            Wynik: Funkcja jest różniczkowalna, a płaszczyzna styczna w $(1, 1)$ to $z = 2x + 2y - 2$.
        
        **Zastosowanie w informatyce**:
        
        - Metody gradientowe w uczeniu maszynowym (np. optymalizacja sieci neuronowych).
        - Modelowanie powierzchni w grafice komputerowej (np. rendering 3D).
        - Rozwiązywanie równań różniczkowych w symulacjach fizycznych.
    2. Zastosowania w informatyce
        
        - Optymalizacja funkcji kosztu w algorytmach uczenia maszynowego.
        - Analiza numeryczna w modelowaniu systemów wielowymiarowych.
        - Projektowanie algorytmów w przetwarzaniu sygnałów i grafice komputerowej.
3. Ekstrema lokalne
    
    1. Definicja i twierdzenia
        
        Ekstrema lokalne funkcji wielu zmiennych to punkty, w których funkcja osiąga lokalne maksimum lub minimum.
        
        **Definicja**:  
        Funkcja $f: \mathbb{R}^n \to \mathbb{R}$ ma lokalne maksimum (minimum) w punkcie $\mathbf{a}$, jeśli istnieje okolica $\mathbf{a}$, taka że $f(\mathbf{x}) \leq f(\mathbf{a})$ ($f(\mathbf{x}) \geq f(\mathbf{a})$) dla wszystkich $\mathbf{x}$ w tej okolicy.
        
        - Warunek konieczny: Jeśli $f$ jest różniczkowalna w $\mathbf{a}$ i $\mathbf{a}$ jest ekstremum lokalnym, to $\nabla f(\mathbf{a}) = \mathbf{0}$ (punkt krytyczny).
        - Warunek wystarczający (test macierzy Hessego): Dla punktu krytycznego $\mathbf{a}$, macierz Hessego $H(\mathbf{a})$ to macierz drugich pochodnych cząstkowych:  
         $$
H(\mathbf{a}) = \left[ \frac{\partial^2 f}{\partial x_i \partial x_j}(\mathbf{a}) \right]_{n \times n}
$$
        - Jeśli $H(\mathbf{a})$ jest dodatnio określona ($x^T H x > 0$ dla $x \neq 0$), to $\mathbf{a}$ jest lokalnym minimum.
        - Jeśli $H(\mathbf{a})$ jest ujemnie określona ($x^T H x < 0$), to $\mathbf{a}$ jest lokalnym maksimum.
        - Jeśli $H(\mathbf{a})$ jest nieokreślona, $\mathbf{a}$ może być punktem siodłowym.
        
        **Twierdzenia**:
        
        - Twierdzenie o punktach krytycznych: Jeśli $\mathbf{a}$ jest ekstremum lokalnym i $f$ jest różniczkowalna w $\mathbf{a}$, to $\nabla f(\mathbf{a}) = \mathbf{0}$.
        - Dla funkcji dwóch zmiennych: Jeśli $\nabla f(a, b) = (0, 0)$ i wyznacznik macierzy Hessego $D = \frac{\partial^2 f}{\partial x^2} \frac{\partial^2 f}{\partial y^2} - \left( \frac{\partial^2 f}{\partial x \partial y} \right)^2$, to:
            - $D > 0$ i $\frac{\partial^2 f}{\partial x^2} > 0$ → lokalne minimum.
            - $D > 0$ i $\frac{\partial^2 f}{\partial x^2} < 0$ → lokalne maksimum.
            - $D < 0$ → punkt siodłowy.
            - $D = 0$ → test nie rozstrzyga.
        
        **Przykład**:  
        Znajdźmy ekstrema lokalne funkcji $f(x, y) = x^2 + y^2 - 2x - 4y + 5$.
        
        - Gradient: $\nabla f(x, y) = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right) = (2x - 2, 2y - 4)$.
        - Punkty krytyczne: $2x - 2 = 0 \implies x = 1$, $2y - 4 = 0 \implies y = 2$. Punkt krytyczny: $(1, 2)$.
        - Macierz Hessego:  
            [  
            H(x, y) = \begin{bmatrix} \frac{\partial^2 f}{\partial x^2} & \frac{\partial^2 f}{\partial x \partial y} \ \frac{\partial^2 f}{\partial y \partial x} & \frac{\partial^2 f}{\partial y^2} \end{bmatrix} = \begin{bmatrix} 2 & 0 \ 0 & 2 \end{bmatrix}.  
            ]
        - Wyznacznik: $D = 2 \cdot 2 - 0 \cdot 0 = 4 > 0$, $\frac{\partial^2 f}{\partial x^2} = 2 > 0$, więc $(1, 2)$ to lokalne minimum.
        - Wartość w minimum: $f(1, 2) = 1^2 + 2^2 - 2 \cdot 1 - 4 \cdot 2 + 5 = 1 + 4 - 2 - 8 + 5 = 0$.  
            Wynik: Lokalne minimum w $(1, 2)$, $f(1, 2) = 0$.
        
        **Zastosowanie w informatyce**:
        
        - Optymalizacja funkcji kosztu w uczeniu maszynowym (np. regresja liniowa, sieci neuronowe).
        - Modelowanie powierzchni w grafice komputerowej (np. minimalizacja energii).
        - Analiza systemów dynamicznych w symulacjach.
    2. Zastosowania w informatyce
        
        - Optymalizacja hiperparametrów w algorytmach uczenia maszynowego.
        - Analiza numeryczna w modelowaniu 3D i symulacjach fizycznych.
        - Projektowanie algorytmów w systemach sterowania i regulacji.
4. Zastosowania w informatyce
    
    - Pochodne cząstkowe: Obliczanie gradientów w algorytmach optymalizacyjnych, przetwarzanie obrazów, analiza numeryczna.
    - Różniczkowalność: Modelowanie powierzchni w grafice komputerowej, optymalizacja w uczeniu maszynowym, symulacje fizyczne.
    - Ekstrema lokalne: Optymalizacja funkcji kosztu, projektowanie algorytmów w grafice komputerowej, analiza systemów dynamicznych.

#### 12. Podstawy rachunku całkowego: całka Riemanna (funkcji jednej i wielu zmiennych), zmiana zmiennych w całce (współrzędne walcowe i sferyczne).

1.  Całka Riemanna dla funkcji jednej zmiennej
	
	#### Definicja i własności
	Całka Riemanna jest podstawowym narzędziem rachunku całkowego, służącym do obliczania pola pod krzywą, sumowania nieskończenie wielu małych przyrostów lub analizy problemów fizycznych.
	
	**Definicja**: Dla funkcji $f: [a, b] \to \mathbb{R}$, która jest ograniczona na przedziale $[a, b]$, całka Riemanna jest zdefiniowana jako granica sum Riemanna:
	$$
	\int_a^b f(x) \, dx = \lim_{|\Delta| \to 0} \sum_{i=1}^n f(x_i^*) \Delta x_i
	$$
	gdzie $\Delta = \{x_0, x_1, \ldots, x_n\}$ to podział przedziału $[a, b]$, $\Delta x_i = x_i - x_{i-1}$, $x_i^* \in [x_{i-1}, x_i]$, a $|\Delta| = \max \Delta x_i$. Funkcja $f$ jest całkowalna, jeśli granica istnieje i jest niezależna od wyboru podziału i punktów $x_i^*$.
	
	**Twierdzenia**:
	*   **Twierdzenie o całkowalności**: Jeśli $f$ jest ciągła na $[a, b]$, to jest całkowalna według Riemanna.
	*   **Podstawowe twierdzenie rachunku całkowego**: Jeśli $f$ jest ciągła na $[a, b]$, a $F$ jest jej funkcją pierwotną ($F' = f$), to:
	    $$
	    \int_a^b f(x) \, dx = F(b) - F(a)
	    $$
	*   **Własności liniowości**: Dla stałej $c$:
	    $$
	    \int_a^b (cf(x) + g(x)) \, dx = c \int_a^b f(x) \, dx + \int_a^b g(x) \, dx
	    $$
	*   **Addytywność względem przedziału**: Dla $c \in [a, b]$:
	    $$
	    \int_a^b f(x) \, dx = \int_a^c f(x) \, dx + \int_c^b f(x) \, dx
	    $$
	
	**Przykład**: Obliczmy $\int_0^1 x^2 \, dx$.
	*   Funkcja pierwotna: $F(x) = \frac{1}{3}x^3$.
	*   Z podstawowego twierdzenia: $\int_0^1 x^2 \, dx = F(1) - F(0) = \frac{1}{3} \cdot 1^3 - \frac{1}{3} \cdot 0^3 = \frac{1}{3}$.
	*   Wynik: $\int_0^1 x^2 \, dx = \frac{1}{3}$.
	
	**Zastosowanie w informatyce**:
	*   Obliczanie pól i długości w grafice komputerowej (np. modelowanie 3D).
	*   Metody numeryczne do obliczania całek (np. metoda trapezów, metoda Simpsona).
	*   Analiza sygnałów (np. transformata Fouriera).
	
2.  Całka Riemanna dla funkcji wielu zmiennych
	
	#### Definicja i własności
	Całka Riemanna dla funkcji wielu zmiennych uogólnia pojęcie całki na obszary w przestrzeni $\mathbb{R}^n$, np. pola powierzchni lub objętości.
	
	**Definicja**: Dla funkcji $f: D \to \mathbb{R}$, gdzie $D \subset \mathbb{R}^n$ jest zbiorem ograniczonym, całka Riemanna to:
	$$
	\int_D f(\mathbf{x}) \, dV = \lim_{|\Delta| \to 0} \sum_{i=1}^k f(\mathbf{x}_i^*) \Delta V_i
	$$
	gdzie $\Delta$ to podział $D$ na podobszary o objętościach $\Delta V_i$, $\mathbf{x}_i^* \in \Delta V_i$, a $|\Delta|$ to maksymalny „rozmiar” podobszaru. Funkcja $f$ jest całkowalna, jeśli granica istnieje. Dla $n=2$, $D \subset \mathbb{R}^2$, całka podwójna: $\iint_D f(x, y) \, dx \, dy$. Dla $n=3$, całka potrójna: $\iiint_D f(x, y, z) \, dx \, dy \, dz$.
	
	**Twierdzenia**:
	*   Jeśli $f$ jest ciągła na ograniczonym i domkniętym zbiorze $D$, to jest całkowalna według Riemanna.
	*   **Twierdzenie Fubiniego**: Jeśli $f$ jest ciągła na prostokącie $D = [a, b] \times [c, d]$, to:
	    $$
	    \iint_D f(x, y) \, dx \, dy = \int_a^b \left( \int_c^d f(x, y) \, dy \right) dx = \int_c^d \left( \int_a^b f(x, y) \, dx \right) dy
	    $$
	
	**Przykład**: Obliczmy $\iint_D x y \, dx \, dy$, gdzie $D = [0, 1] \times [0, 1]$.
	Z twierdzenia Fubiniego:
	$$
	\int_0^1 \left( \int_0^1 xy \, dy \right) dx = \int_0^1 x \left[ \frac{y^2}{2} \right]_0^1 \, dx = \int_0^1 x \cdot \frac{1}{2} \, dx = \frac{1}{2} \left[ \frac{x^2}{2} \right]_0^1 = \frac{1}{4}
	$$
	Wynik: $\iint_D xy \, dx \, dy = \frac{1}{4}$.
	
	**Zastosowanie w informatyce**:
	*   Obliczanie momentów bezwładności w symulacjach fizycznych.
	*   Analiza obrazów i przetwarzanie sygnałów (np. całkowanie w przestrzeni 2D/3D).
	*   Obliczenia numeryczne w modelowaniu wielowymiarowym (np. metoda Monte Carlo).
	
3. Zmiana zmiennych w całce
	
	#### Zmiana zmiennych: współrzędne walcowe i sferyczne
	Zmiana zmiennych w całce pozwala uprościć obliczanie całek wielokrotnych przez przejście na bardziej odpowiednie układy współrzędnych, uwzględniając jakobian transformacji.
	
	**Definicja**: Dla funkcji $f: \mathbb{R}^n \to \mathbb{R}$ i przekształcenia $\mathbf{x} = \mathbf{g}(\mathbf{u})$ z $\mathbb{R}^n$ do $\mathbb{R}^n$, całka zmienia się według wzoru:
	$$
	\int_D f(\mathbf{x}) \, dV = \int_{\mathbf{g}^{-1}(D)} f(\mathbf{g}(\mathbf{u})) |\det J_{\mathbf{g}}(\mathbf{u})| \, dU
	$$
	gdzie $J_{\mathbf{g}}$ to macierz jakobianu przekształcenia $\mathbf{g}$, a $|\det J_{\mathbf{g}}|$ to bezwzględna wartość wyznacznika.
	
	**Współrzędne walcowe**: Dla przestrzeni $\mathbb{R}^3$, współrzędne walcowe to $(r, \theta, z)$, gdzie:
	*   $x = r \cos \theta$, $y = r \sin \theta$, $z = z$
	*   Jakobian: $|\det J| = r$
	*   Element objętości: $dx \, dy \, dz = r \, dr \, d\theta \, dz$.
	Współrzędne walcowe są użyteczne dla obszarów z symetrią walcową, np. cylindrów.
	
	**Przykład (współrzędne walcowe)**: Obliczmy objętość walca $x^2 + y^2 \leq 1$, $0 \leq z \leq 1$.
	*   W układzie walcowym: $D = \{(r, \theta, z) : 0 \leq r \leq 1, 0 \leq \theta \leq 2\pi, 0 \leq z \leq 1\}$.
	*   Całka: $\iiint_D 1 \, dx \, dy \, dz = \int_0^1 \int_0^{2\pi} \int_0^1 r \, dr \, d\theta \, dz$.
	*   Obliczenia:
	    $$
	    \int_0^1 \left( \int_0^{2\pi} \left( \int_0^1 r \, dr \right) d\theta \right) dz = \int_0^1 \left( \int_0^{2\pi} \left[ \frac{r^2}{2} \right]_0^1 d\theta \right) dz = \int_0^1 \left( \int_0^{2\pi} \frac{1}{2} \, d\theta \right) dz = \int_0^1 \pi \, dz = \pi
	    $$
	*   Wynik: Objętość walca wynosi $\pi$.
	
	**Współrzędne sferyczne**: Dla przestrzeni $\mathbb{R}^3$, współrzędne sferyczne to $(\rho, \theta, \phi)$, gdzie:
	*   $x = \rho \sin \phi \cos \theta$, $y = \rho \sin \phi \sin \theta$, $z = \rho \cos \phi$
	*   Jakobian: $|\det J| = \rho^2 \sin \phi$
	*   Element objętości: $dx \, dy \, dz = \rho^2 \sin \phi \, d\rho \, d\theta \, d\phi$.
	Współrzędne sferyczne są użyteczne dla obszarów z symetrią kulistą, np. kul.
	
	**Przykład (współrzędne sferyczne)**: Obliczmy objętość kuli $x^2 + y^2 + z^2 \leq 1$.
	*   W układzie sferycznym: $D = \{(\rho, \theta, \phi) : 0 \leq \rho \leq 1, 0 \leq \theta \leq 2\pi, 0 \leq \phi \leq \pi\}$.
	*   Całka: $\iiint_D 1 \, dx \, dy \, dz = \int_0^\pi \int_0^{2\pi} \int_0^1 \rho^2 \sin \phi \, d\rho \, d\theta \, d\phi$.
	*   Obliczenia:
	    $$
	    \int_0^\pi \left( \int_0^{2\pi} \sin \phi \left[ \frac{\rho^3}{3} \right]_0^1 d\theta \right) d\phi = \int_0^\pi \left( \int_0^{2\pi} \frac{1}{3} \sin \phi \, d\theta \right) d\phi = \int_0^\pi \frac{2\pi}{3} \sin \phi \, d\phi = \frac{2\pi}{3} [-\cos \phi]_0^\pi = \frac{4\pi}{3}
	    $$
	*   Wynik: Objętość kuli wynosi $\frac{4}{3}\pi$.
	
	**Zastosowanie w informatyce**:
	*   Modelowanie obiektów 3D w grafice komputerowej (np. rendering kul, cylindrów).
	*   Symulacje fizyczne (np. pola grawitacyjne, elektromagnetyczne).
	*   Analiza numeryczna w problemach z symetrią (np. metoda elementów skończonych).
