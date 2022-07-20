---
title: Clear
second_title: Aspose.Words für .NET-API-Referenz
description: Entfernt alle Elemente aus der Sammlung.
type: docs
weight: 40
url: /de/net/aspose.words.markup/customxmlschemacollection/clear/
---
## CustomXmlSchemaCollection.Clear method

Entfernt alle Elemente aus der Sammlung.

```csharp
public void Clear()
```

### Beispiele

Zeigt, wie mit einer XML-Schemaauflistung gearbeitet wird.

```csharp
Document doc = new Document();

string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello, World!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

// Eine XML-Schemazuordnung hinzufügen.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Klonen Sie die XML-Schemazuordnungssammlung des benutzerdefinierten XML-Teils,
// und fügen Sie dem Klon dann ein paar neue Schemas hinzu.
CustomXmlSchemaCollection schemas = xmlPart.Schemas.Clone();
schemas.Add("http://www.w3.org/2001/XMLSchema-Instanz");
schemas.Add("http://schemas.microsoft.com/office/2006/metadata/contentType");

Assert.AreEqual(3, schemas.Count);
Assert.AreEqual(2, schemas.IndexOf("http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Die Schemas aufzählen und jedes Element drucken.
using (IEnumerator<string> enumerator = schemas.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine(enumerator.Current);
}

// Im Folgenden finden Sie drei Möglichkeiten zum Entfernen von Schemas aus der Sammlung.
// 1 - Entfernen Sie ein Schema nach Index:
schemas.RemoveAt(2);

// 2 - Schema nach Wert entfernen:
schemas.Remove("http://www.w3.org/2001/XMLSchema");

// 3 - Verwenden Sie die "Clear"-Methode, um die Sammlung sofort zu leeren.
schemas.Clear();

Assert.AreEqual(0, schemas.Count);
```

### Siehe auch

* class [CustomXmlSchemaCollection](../../customxmlschemacollection)
* namensraum [Aspose.Words.Markup](../../customxmlschemacollection)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->