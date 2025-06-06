---
title: DropDownItemCollection Class
linktitle: DropDownItemCollection
articleTitle: DropDownItemCollection
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Fields.DropDownItemCollection la soluzione ideale per gestire senza sforzo gli elementi a discesa nei campi dei moduli!
type: docs
weight: 1910
url: /it/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

Una raccolta di stringhe che rappresentano tutti gli elementi in un campo di un modulo a discesa.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Ottiene il numero di elementi contenuti nella raccolta. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Ottiene o imposta l'elemento all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(*string*) | Aggiunge una stringa alla fine della raccolta. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Rimuove tutti gli elementi dalla raccolta. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(*string*) | Determina se la raccolta contiene il valore specificato. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Restituisce un oggetto enumeratore che può essere utilizzato per scorrere tutti gli elementi nella raccolta. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(*string*) | Restituisce l'indice basato su zero del valore specificato nella raccolta. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(*int, string*) | Inserisce una stringa nella raccolta all'indice specificato. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(*string*) | Rimuove il valore specificato dalla raccolta. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(*int*) | Rimuove un valore all'indice specificato. |

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

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
