---
title: CustomXmlPropertyCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words für .NET
description: Löschen Sie Ihre CustomXmlPropertyCollection mühelos mit der Clear-Methode und entfernen Sie alle Elemente für eine optimierte Datenverwaltung.
type: docs
weight: 40
url: /de/net/aspose.words.markup/customxmlpropertycollection/clear/
---
## CustomXmlPropertyCollection.Clear method

Entfernt alle Elemente aus der Sammlung.

```csharp
public void Clear()
```

## Beispiele

Zeigt, wie Sie mit Smarttag-Eigenschaften arbeiten, um ausführliche Informationen zu Smarttags zu erhalten.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Ein Smarttag erscheint in einem Dokument, in dem Microsoft Word einen Teil des Textes als eine Art Daten erkennt.
// wie etwa einen Namen, ein Datum oder eine Adresse, und wandelt es in einen Hyperlink um, der eine violette gepunktete Unterstreichung anzeigt.
// In Word 2003 können wir Smarttags über „Extras“ -> „AutoKorrektur-Optionen…“ -> „SmartTags“ aktivieren.
// In unserem Eingabedokument gibt es drei Objekte, die Microsoft Word als Smarttags registriert hat.
// Smarttags können verschachtelt sein, daher enthält diese Sammlung mehr.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// Das Element „Eigenschaften“ eines Smarttags enthält dessen Metadaten, die für jeden Smarttag-Typ unterschiedlich sind.
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

// Wir können auf die Eigenschaften auch auf verschiedene Weise zugreifen, beispielsweise über ein Schlüssel-Wert-Paar.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// Unten sind drei Möglichkeiten zum Entfernen von Elementen aus der Eigenschaftensammlung aufgeführt.
// 1 - Entfernen nach Index:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Löschen Sie die gesamte Sammlung auf einmal:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [CustomXmlPropertyCollection](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
