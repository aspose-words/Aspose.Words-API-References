---
title: CustomXmlSchemaCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: CustomXmlSchemaCollection Remove methode. Entfernt den angegebenen Wert aus der Sammlung in C#.
type: docs
weight: 80
url: /de/net/aspose.words.markup/customxmlschemacollection/remove/
---
## CustomXmlSchemaCollection.Remove method

Entfernt den angegebenen Wert aus der Sammlung.

```csharp
public void Remove(string name)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der zu entfernende Wert, bei dem die Groß-/Kleinschreibung beachtet werden soll. |

## Beispiele

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
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
