---
title: PersonCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Rimuovi facilmente una persona dalla tua raccolta con il metodo PersonCollection Remove. Semplifica la gestione dei tuoi dati oggi stesso!
type: docs
weight: 70
url: /it/net/aspose.words.bibliography/personcollection/remove/
---
## PersonCollection.Remove method

Rimuove la persona dalla raccolta.

```csharp
public bool Remove(Person person)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| person | Person | La persona da rimuovere dalla collezione. |

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
