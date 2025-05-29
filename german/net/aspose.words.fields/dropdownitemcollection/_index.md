---
title: DropDownItemCollection Class
linktitle: DropDownItemCollection
articleTitle: DropDownItemCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Fields.DropDownItemCollection – Ihre Lösung für die mühelose Verwaltung von Dropdown-Elementen in Formularfeldern!
type: docs
weight: 1910
url: /de/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

Eine Sammlung von Zeichenfolgen, die alle Elemente in einem Dropdown-Formularfeld darstellen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Feldern](https://docs.aspose.com/words/net/working-with-fields/) Dokumentationsartikel.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Ruft das Element am angegebenen Index ab oder legt es fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(*string*) | Fügt am Ende der Sammlung eine Zeichenfolge hinzu. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(*string*) | Bestimmt, ob die Sammlung den angegebenen Wert enthält. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(*string*) | Gibt den nullbasierten Index des angegebenen Werts in der Auflistung zurück. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(*int, string*) | Fügt eine Zeichenfolge am angegebenen Index in die Sammlung ein. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(*string*) | Entfernt den angegebenen Wert aus der Sammlung. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(*int*) | Entfernt einen Wert am angegebenen Index. |

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

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* namensraum [Aspose.Words.Fields](../../aspose.words.fields/)
* Montage [Aspose.Words](../../)
