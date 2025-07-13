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
	Wyróżniamy dwa typy kolejek - Tablicę cykliczną i Listę wiązaną