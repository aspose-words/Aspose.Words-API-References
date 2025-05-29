---
title: DropDownItemCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words per .NET
description: Scopri se una DropDownItemCollection include il valore specificato con il nostro efficiente metodo Contains. Migliora la gestione dei tuoi dati senza sforzo!
type: docs
weight: 50
url: /it/net/aspose.words.fields/dropdownitemcollection/contains/
---
## DropDownItemCollection.Contains method

Determina se la raccolta contiene il valore specificato.

```csharp
public bool Contains(string value)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | String | Valore da individuare, con distinzione tra maiuscole e minuscole. |

### Valore di ritorno

`VERO`se l'elemento si trova nella raccolta; in caso contrario,`falso`.

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
