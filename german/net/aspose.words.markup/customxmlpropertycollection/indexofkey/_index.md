---
title: CustomXmlPropertyCollection.IndexOfKey
second_title: Aspose.Words für .NET-API-Referenz
description: CustomXmlPropertyCollection methode. Gibt den nullbasierten Index der angegebenen Eigenschaft in der Sammlung zurück.
type: docs
weight: 70
url: /de/net/aspose.words.markup/customxmlpropertycollection/indexofkey/
---
## CustomXmlPropertyCollection.IndexOfKey method

Gibt den nullbasierten Index der angegebenen Eigenschaft in der Sammlung zurück.

```csharp
public int IndexOfKey(string name)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der Eigenschaft, bei dem die Groß-/Kleinschreibung beachtet wird. |

### Rückgabewert

Der auf Null basierende Index. Negativer Wert, wenn nicht gefunden.

### Beispiele

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

* class [CustomXmlPropertyCollection](../)
* namensraum [Aspose.Words.Markup](../../customxmlpropertycollection/)
* Montage [Aspose.Words](../../../)


