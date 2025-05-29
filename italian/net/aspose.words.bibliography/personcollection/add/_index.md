---
title: PersonCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words per .NET
description: Aggiungi facilmente una persona alla tua collezione con il metodo PersonCollection Add. Semplifica la gestione dei dati e migliora l'efficienza del tuo progetto!
type: docs
weight: 40
url: /it/net/aspose.words.bibliography/personcollection/add/
---
## PersonCollection.Add method

Aggiunge un[`Person`](../../person/) alla collezione.

```csharp
public void Add(Person person)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| person | Person | La persona da aggiungere alla collezione. |

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
