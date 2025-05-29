---
title: CustomXmlSchemaCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: Entdecken Sie die CustomXmlSchemaCollection GetEnumerator-Methode, um alle Sammlungselemente einfach zu durchlaufen. Optimieren Sie noch heute Ihr XML-Datenmanagement!
type: docs
weight: 60
url: /de/net/aspose.words.markup/customxmlschemacollection/getenumerator/
---
## CustomXmlSchemaCollection.GetEnumerator method

Gibt ein Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können.

```csharp
public IEnumerator<string> GetEnumerator()
```

## Beispiele

Zeigt, wie mit einer XML-Schemasammlung gearbeitet wird.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Eine XML-Schemazuordnung hinzufügen.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Klonen Sie die XML-Schema-Assoziationssammlung des benutzerdefinierten XML-Teils.
// und fügen Sie dem Klon dann ein paar neue Schemata hinzu.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-instance");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Schemata aufzählen und jedes Element drucken.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Unten sind drei Möglichkeiten zum Entfernen von Schemas aus der Sammlung aufgeführt.
// 1 – Entfernen Sie ein Schema nach Index:
schemas.RemoveAt(2);

// 2 – Entfernen Sie ein Schema nach Wert:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Verwenden Sie die Methode „Clear“, um die Sammlung sofort zu leeren.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Siehe auch

* class [CustomXmlSchemaCollection](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
