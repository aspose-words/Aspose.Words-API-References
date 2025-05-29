---
title: PersonCollection
linktitle: PersonCollection
articleTitle: PersonCollection
second_title: Aspose.Words per .NET
description: Crea e gestisci una raccolta dinamica di individui con la classe PersonCollection. Semplifica la gestione dei dati e migliora le tue applicazioni oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection() {#constructor}

Inizializza una nuova istanza di[`PersonCollection`](../) classe.

```csharp
public PersonCollection()
```

## Esempi

Mostra come lavorare con la raccolta di persone.

```csharp
// Crea una nuova raccolta di persone.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Aggiungi una nuova persona alla raccolta.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Rimuove la persona dalla raccolta se esiste.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// Crea una raccolta di persone con due persone.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Rimuove la persona dalla raccolta in base all'indice.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Rimuovi tutte le persone dalla raccolta.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Guarda anche

* class [PersonCollection](../)
* spazio dei nomi [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assemblea [Aspose.Words](../../../)

---

## PersonCollection(*IEnumerable&lt;Person&gt;*) {#constructor_2}

```csharp
public PersonCollection(IEnumerable<Person> persons)
```

### Guarda anche

* class [Person](../../person/)
* class [PersonCollection](../)
* spazio dei nomi [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assemblea [Aspose.Words](../../../)

---

## PersonCollection(*params Person[]*) {#constructor_1}

Inizializza una nuova istanza di[`PersonCollection`](../) classe.

```csharp
public PersonCollection(params Person[] persons)
```

## Esempi

Mostra come lavorare con la raccolta di persone.

```csharp
// Crea una nuova raccolta di persone.
PersonCollection persons = new PersonCollection();
Person person = new Person("Roxanne", "Brielle", "Tejeda_updated");
// Aggiungi una nuova persona alla raccolta.
persons.Add(person);
Assert.AreEqual(1, persons.Count);
// Rimuove la persona dalla raccolta se esiste.
if (persons.Contains(person))
    persons.Remove(person);
Assert.AreEqual(0, persons.Count);

// Crea una raccolta di persone con due persone.
persons = new PersonCollection(new Person[] { new Person("Roxanne_1", "Brielle_1", "Tejeda_1"), new Person("Roxanne_2", "Brielle_2", "Tejeda_2") });
Assert.AreEqual(2, persons.Count);
// Rimuove la persona dalla raccolta in base all'indice.
persons.RemoveAt(0);
Assert.AreEqual(1, persons.Count);
// Rimuovi tutte le persone dalla raccolta.
persons.Clear();
Assert.AreEqual(0, persons.Count);
```

### Guarda anche

* class [Person](../../person/)
* class [PersonCollection](../)
* spazio dei nomi [Aspose.Words.Bibliography](../../../aspose.words.bibliography/)
* assemblea [Aspose.Words](../../../)
