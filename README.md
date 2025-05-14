# 🧪 MongoDB - Laboratorium 2: Zadania projektowe

## 🎯 Cel

Celem tego ćwiczenia jest przekształcenie relacyjnej bazy danych Chinook na dokumentowy model MongoDB. Studenci mają zaproponować strukturę dokumentów, która będzie logiczna, wydajna i dobrze dopasowana do przypadków użycia.

## 📚 Kontekst

Baza danych Chinook jest przykładową relacyjną bazą danych zawierającą informacje o:

* klientach,
* pracownikach,
* albumach i wykonawcach,
* utworach, gatunkach i mediach,
* zamówieniach i fakturach.

Zadaniem jest zrozumienie tych danych i zaprojektowanie nowej, dokumentowej struktury.

## 🧠 Zadania do wykonania

### 🔹 Zadanie 1: Identyfikacja encji i relacji

Przeanalizuj strukturę relacyjnej bazy Chinook. Wypisz najważniejsze encje oraz relacje między nimi (np. Album → Artist, Invoice → Customer).

### 🔹 Zadanie 2: Zaproponuj strukturę dokumentów

Dla każdej głównej encji zaproponuj przykładową strukturę dokumentu MongoDB w formacie JSON. Przemyśl:

* Które dane warto osadzić (embed),
* Gdzie warto stosować referencje (reference).

---

## 📝 Wskazówki

* Nie odwzorowuj jeden-do-jednego tabel SQL na kolekcje MongoDB — myśl w kategoriach dokumentów i przypadków użycia.
* Pamiętaj, że MongoDB nie wspiera JOINów w klasycznym rozumieniu — projektuj z myślą o zapytaniach.

> 💡 **Na koniec:** przygotuj graficzną mapę kolekcji i ich powiązań (np. jako diagram online).
>
> 👉 Polecane narzędzie: [Hackolade Studio (online)](https://studio.hackolade.com/) — darmowy i dedykowany edytor modelu dokumentowego MongoDB z możliwością tworzenia zagnieżdżonych struktur oraz relacji między kolekcjami.


---
