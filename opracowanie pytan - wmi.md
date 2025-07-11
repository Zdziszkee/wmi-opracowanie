
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
