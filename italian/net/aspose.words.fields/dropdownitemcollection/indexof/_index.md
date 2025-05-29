---
title: DropDownItemCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words per .NET
description: Scopri il metodo IndexOf di DropDownItemCollection, trova in modo efficiente l'indice a partire da zero di qualsiasi valore nella tua raccolta per una gestione semplificata dei dati.
type: docs
weight: 70
url: /it/net/aspose.words.fields/dropdownitemcollection/indexof/
---
## DropDownItemCollection.IndexOf method

Restituisce l'indice basato su zero del valore specificato nella raccolta.

```csharp
public int IndexOf(string value)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | String | Valore da individuare, con distinzione tra maiuscole e minuscole. |

### Valore di ritorno

Indice a base zero. Valore negativo se non trovato.

## Esempi

Mostra come inserire un campo casella combinata e modificare gli elementi nella sua raccolta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce una casella combinata e quindi verifica la raccolta di elementi a discesa.
// In Microsoft Word, l'utente farà clic sulla casella combinata,
// e quindi seleziona uno degli elementi di testo nella raccolta da visualizzare.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Esistono due modi per aggiungere un nuovo elemento a una raccolta esistente di elementi del menu a discesa.
// 1 - Aggiungi un elemento alla fine della raccolta:
dropDownItems.Add("Four");

// 2 - Inserisce un elemento prima di un altro elemento a un indice specificato:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Esegui l'iterazione sulla raccolta e stampa ogni elemento.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Esistono due modi per rimuovere elementi da una raccolta di voci a discesa.
// 1 - Rimuove un elemento con contenuto uguale alla stringa passata:
dropDownItems.Remove("Four");

// 2 - Rimuovi un elemento da un indice:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Svuota l'intera raccolta di elementi a discesa.
dropDownItems.Clear();
```

### Guarda anche

* class [DropDownItemCollection](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
