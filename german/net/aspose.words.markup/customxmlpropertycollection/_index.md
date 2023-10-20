---
title: CustomXmlPropertyCollection Class
linktitle: CustomXmlPropertyCollection
articleTitle: CustomXmlPropertyCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.Markup.CustomXmlPropertyCollection klas. Stellt eine Sammlung benutzerdefinierter XMLAttribute oder SmartTagEigenschaften dar in C#.
type: docs
weight: 3950
url: /de/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

Stellt eine Sammlung benutzerdefinierter XML-Attribute oder Smart-Tag-Eigenschaften dar.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltskontrolle](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | Ruft eine Eigenschaft mit dem angegebenen Namen ab. (2 indexers) |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(*[CustomXmlProperty](../customxmlproperty/)*) | Fügt der Sammlung eine Eigenschaft hinzu. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(*string*) | Bestimmt, ob die Sammlung eine Eigenschaft mit dem angegebenen Namen enthält. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(*string*) | Gibt den nullbasierten Index der angegebenen Eigenschaft in der Sammlung zurück. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(*string*) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(*int*) | Entfernt eine Eigenschaft am angegebenen Index. |

## Bemerkungen

Artikel sind[`CustomXmlProperty`](../customxmlproperty/) Objekte.

## Beispiele

Zeigt, wie Sie mit Smart-Tag-Eigenschaften arbeiten, um detaillierte Informationen zu Smart-Tags zu erhalten.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Ein Smarttag erscheint in einem Dokument, wobei Microsoft Word einen Teil seines Textes als irgendeine Form von Daten erkennt.
// beispielsweise einen Namen, ein Datum oder eine Adresse und wandelt ihn in einen Hyperlink um, der eine violette gepunktete Unterstreichung anzeigt.
// In Word 2003 können wir Smarttags über „Extras“ -> aktivieren. „AutoKorrektur-Optionen…“ -> „SmartTags“.
// In unserem Eingabedokument gibt es drei Objekte, die Microsoft Word als Smarttags registriert hat.
// Smart-Tags können verschachtelt sein, daher enthält diese Sammlung mehr.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Das „Properties“-Mitglied eines Smart-Tags enthält seine Metadaten, die für jeden Smart-Tag-Typ unterschiedlich sind.
// Die Eigenschaften eines Smarttags vom Typ „Datum“ enthalten Jahr, Monat und Tag.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// Wir können auch auf verschiedene Weise auf die Eigenschaften zugreifen, beispielsweise über ein Schlüssel-Wert-Paar.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Nachfolgend finden Sie drei Möglichkeiten, Elemente aus der Eigenschaftensammlung zu entfernen.
// 1 - Nach Index entfernen:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 – Die gesamte Sammlung auf einmal löschen:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [CustomXmlProperty](../customxmlproperty/)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
