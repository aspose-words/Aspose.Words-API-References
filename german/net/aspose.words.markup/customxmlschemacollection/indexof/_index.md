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

Der nullbasierte Index. Negativer Wert, wenn nicht gefunden.

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

* class [CustomXmlSchemaCollection](../)
* namensraum [Aspose.Words.Markup](../../customxmlschemacollection/)
* Montage [Aspose.Words](../../../)


