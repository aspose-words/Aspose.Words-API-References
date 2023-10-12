---
title: CustomXmlSchemaCollection.IndexOf
second_title: Aspose.Words für .NET-API-Referenz
description: CustomXmlSchemaCollection methode. Gibt den nullbasierten Index des angegebenen Werts in der Sammlung zurück.
type: docs
weight: 70
url: /de/net/aspose.words.markup/customxmlschemacollection/indexof/
---
## CustomXmlSchemaCollection.IndexOf method

Gibt den nullbasierten Index des angegebenen Werts in der Sammlung zurück.

```csharp
public int IndexOf(string value)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | String | Der zu suchende Wert, bei dem die Groß-/Kleinschreibung beachtet werden soll. |

### Rückgabewert

Der auf Null basierende Index. Negativer Wert, wenn nicht gefunden.

### Beispiele

Zeigt, wie mit einer XML-Schemasammlung gearbeitet wird.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Eine XML-Schema-Zuordnung hinzufügen.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Klonen Sie die XML-Schema-Zuordnungssammlung des benutzerdefinierten XML-Teils.
// und dann ein paar neue Schemata zum Klon hinzufügen.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Zählen Sie die Schemata auf und drucken Sie jedes Element aus.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Nachfolgend finden Sie drei Möglichkeiten, Schemata aus der Sammlung zu entfernen.
// 1 – Ein Schema nach Index entfernen:
schemas.RemoveAt(2);

// 2 – Ein Schema nach Wert entfernen:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 – Verwenden Sie die Methode „Clear“, um die Sammlung sofort zu leeren.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Siehe auch

* class [CustomXmlSchemaCollection](../)
* namensraum [Aspose.Words.Markup](../../customxmlschemacollection/)
* Montage [Aspose.Words](../../../)


