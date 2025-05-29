---
title: DropDownItemCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Mit der DropDownItemCollection-Elementeigenschaft können Sie mühelos auf Elemente zugreifen und diese verwalten. Legen Sie Elemente nach Index fest oder rufen Sie sie ab, um eine nahtlose Datenverarbeitung zu gewährleisten.
type: docs
weight: 20
url: /de/net/aspose.words.fields/dropdownitemcollection/item/
---
## DropDownItemCollection indexer

Ruft das Element am angegebenen Index ab oder legt es fest.

```csharp
public string this[int index] { get; set; }
```

## Beispiele

Zeigt, wie Sie ein Kombinationsfeld einfügen und die Elemente in seiner Elementsammlung bearbeiten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein Kombinationsfeld ein und überprüfen Sie dann die darin enthaltenen Dropdown-Elemente.
// In Microsoft Word klickt der Benutzer auf das Kombinationsfeld,
// und wählen Sie dann eines der Textelemente in der Sammlung zur Anzeige aus.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Es gibt zwei Möglichkeiten, einer vorhandenen Sammlung von Dropdown-Box-Elementen ein neues Element hinzuzufügen.
// 1 – Ein Element an das Ende der Sammlung anhängen:
dropDownItems.Add("Four");

// 2 – Fügen Sie ein Element vor einem anderen Element an einem angegebenen Index ein:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Durchlaufe die Sammlung und drucke jedes Element.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Es gibt zwei Möglichkeiten, Elemente aus einer Sammlung von Dropdown-Elementen zu entfernen.
// 1 – Entfernt ein Element mit dem Inhalt der übergebenen Zeichenfolge:
dropDownItems.Remove("Four");

// 2 - Entfernen Sie ein Element an einem Index:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Leere die gesamte Sammlung der Dropdown-Elemente.
dropDownItems.Clear();
```

### Siehe auch

* class [DropDownItemCollection](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
