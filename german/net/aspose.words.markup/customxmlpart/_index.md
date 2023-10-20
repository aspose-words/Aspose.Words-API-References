---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words für .NET
description: Aspose.Words.Markup.CustomXmlPart klas. Stellt einen benutzerdefinierten XMLDatenspeicherteil dar benutzerdefinierte XMLDaten innerhalb eines Pakets in C#.
type: docs
weight: 3920
url: /de/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Stellt einen benutzerdefinierten XML-Datenspeicherteil dar (benutzerdefinierte XML-Daten innerhalb eines Pakets).

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltskontrolle](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class CustomXmlPart
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Ruft den XML-Inhalt dieses benutzerdefinierten XML-Datenspeicherteils ab oder legt ihn fest. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Gibt eine CRC-Prüfsumme (Cyclic Redundancy Check) des an[`Data`](./data/) Inhalt. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Ruft die Zeichenfolge ab, die diesen benutzerdefinierten XML-Teil in einem OOXML-Dokument identifiziert, oder legt diese fest. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Gibt den Satz von XML-Schemas an, die diesem benutzerdefinierten XML-Teil zugeordnet sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Erstellt eine ausreichend tiefe Kopie des Objekts. Dupliziert nicht die Bytes von[`Data`](./data/) value. |

## Bemerkungen

Ein DOCX- oder DOC-Dokument kann einen oder mehrere benutzerdefinierte XML-Datenspeicherteile enthalten. Aspose.Words bewahrt und ermöglicht das Erstellen und Extrahieren benutzerdefinierter XML-Daten über das[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) Sammlung.

## Beispiele

Zeigt, wie ein strukturiertes Dokument-Tag mit benutzerdefinierten XML-Daten erstellt wird.

```csharp
Document doc = new Document();

// Einen XML-Teil erstellen, der Daten enthält, und ihn der Sammlung des Dokuments hinzufügen.
// Wenn wir die Registerkarte „Entwickler“ in Microsoft Word aktivieren,
// Elemente aus dieser Sammlung finden wir im „XML Mapping Pane“, zusammen mit einigen Standardelementen.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Nachfolgend finden Sie zwei Möglichkeiten, auf XML-Teile zu verweisen.
// 1 – Durch einen Index in der benutzerdefinierten XML-Teilesammlung:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Nach GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Eine XML-Schema-Zuordnung hinzufügen.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Ein Teil klonen und es dann in die Sammlung einfügen.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Durchlaufen Sie die Sammlung und drucken Sie den Inhalt jedes Teils aus.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Verwenden Sie die Methode „RemoveAt“, um den geklonten Teil nach Index zu entfernen.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Klonen Sie die XML-Teilesammlung und entfernen Sie dann mit der Methode „Clear“ alle Elemente auf einmal.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Erstellen Sie ein strukturiertes Dokument-Tag, das den Inhalt unseres Teils anzeigt, und fügen Sie ihn in den Dokumentkörper ein.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
