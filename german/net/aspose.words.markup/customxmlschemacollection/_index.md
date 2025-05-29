---
title: CustomXmlSchemaCollection Class
linktitle: CustomXmlSchemaCollection
articleTitle: CustomXmlSchemaCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Markup.CustomXmlSchemaCollection zum Verwalten von XML-Schemas, die mit benutzerdefinierten XML-Teilen verknüpft sind, und verbessern Sie so die Dokumentflexibilität und -kontrolle.
type: docs
weight: 4650
url: /de/net/aspose.words.markup/customxmlschemacollection/
---
## CustomXmlSchemaCollection class

Eine Sammlung von Zeichenfolgen, die XML-Schemas darstellen, die einem benutzerdefinierten XML-Teil zugeordnet sind.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class CustomXmlSchemaCollection : IEnumerable<string>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlschemacollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.markup/customxmlschemacollection/item/) { get; set; } | Ruft das Element am angegebenen Index ab oder legt es fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlschemacollection/add/)(*string*) | Fügt der Sammlung ein Element hinzu. |
| [Clear](../../aspose.words.markup/customxmlschemacollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Clone](../../aspose.words.markup/customxmlschemacollection/clone/)() | Erstellt einen tiefen Klon dieses Objekts. |
| [GetEnumerator](../../aspose.words.markup/customxmlschemacollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können. |
| [IndexOf](../../aspose.words.markup/customxmlschemacollection/indexof/)(*string*) | Gibt den nullbasierten Index des angegebenen Werts in der Auflistung zurück. |
| [Remove](../../aspose.words.markup/customxmlschemacollection/remove/)(*string*) | Entfernt den angegebenen Wert aus der Sammlung. |
| [RemoveAt](../../aspose.words.markup/customxmlschemacollection/removeat/)(*int*) | Entfernt einen Wert am angegebenen Index. |

## Bemerkungen

Sie erstellen keine Instanzen dieser Klasse. Sie greifen auf die Sammlung von XML-Schemata eines benutzerdefinierten XML-Teils über die[`Schemas`](../customxmlpart/schemas/) Eigentum.

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
