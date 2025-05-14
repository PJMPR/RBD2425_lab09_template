# 🧪 MongoDB – Laboratorium 1: Podstawowe komendy (z DataGrip)

Ten dokument zawiera zestaw podstawowych komend MongoDB, które każdy student powinien znać na początek pracy z tą bazą danych. Komendy są przeznaczone do użycia w **DataGrip**, w zakładce terminala lub bezpośrednio w oknie zapytań do MongoDB.

---

## 🧭 Praca z MongoDB w DataGrip

1. Skonfiguruj połączenie z MongoDB (host: `localhost`, port: `27017`, user: `admin`, password: `haslo123`, Auth DB: `admin`).
2. Po połączeniu:
   - możesz kliknąć prawym przyciskiem myszy na nazwę połączenia → `Jump to Console`
   - lub otworzyć `New → Mongo Console`, gdzie wpiszesz poniższe polecenia.

---

## 📁 Operacje na bazach i kolekcjach

```js
show dbs                        // list databases
use my_database                 // switch to or create database
db.createCollection("clients")  // create a new collection
show collections                // list collections
```

---

## 🟩 CREATE – dodawanie danych

```js
db.clients.insertOne({ firstName: "Jan", lastName: "Kowalski", age: 30 })

db.clients.insertMany([
  { firstName: "Anna", lastName: "Nowak", age: 25 },
  { firstName: "Piotr", lastName: "Zieliński", age: 40 }
])
```

---

## 🔍 READ – wyszukiwanie danych

```js
db.clients.find()                                // find all documents
db.clients.find({ firstName: "Jan" })            // filter by field
db.clients.findOne({ age: { $gt: 30 } })         // one document where age > 30
db.clients.find().pretty()                       // formatted output
```

---

## ✏️ UPDATE – modyfikacja danych

```js
db.clients.updateOne(
  { firstName: "Jan" },
  { $set: { age: 31 } }
)

db.clients.updateMany(
  { age: { $lt: 30 } },
  { $set: { category: "young" } }
)
```

---

## 🗑️ DELETE – usuwanie danych

```js
db.clients.deleteOne({ firstName: "Jan" })
db.clients.deleteMany({ age: { $gt: 60 } })
```

---

## 🧠 Komendy administracyjne

```js
db.clients.countDocuments()    // count documents in collection
db.dropDatabase()              // drop entire database
```

---

## 🎓 Zadania do wykonania

1. **Utwórz nową bazę danych o nazwie `shop` oraz kolekcję `products`.**
2. **Dodaj do kolekcji `products` trzy dokumenty opisujące produkt (np. name, price, category).**
3. **Wyszukaj wszystkie produkty z ceną większą niż 50.**
4. **Zaktualizuj kategorię jednego z produktów na `promo`.**
5. **Usuń wszystkie produkty, których cena jest mniejsza niż 10.**
6. **Policz, ile dokumentów znajduje się obecnie w kolekcji `products`.**
7. **Dodaj dokument z polem typu tablica, np. `tags: ["new", "popular"]`.**
8. **Wyszukaj dokumenty, które zawierają konkretny element w tablicy (`tags: "popular"`).**

---
