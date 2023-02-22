---
title: Class CustomXmlPart
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Markup.CustomXmlPart klas. Repräsentiert einen benutzerdefinierten XMLDatenspeicherteil benutzerdefinierte XMLDaten innerhalb eines Pakets.
type: docs
weight: 3680
url: /de/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Repräsentiert einen benutzerdefinierten XML-Datenspeicherteil (benutzerdefinierte XML-Daten innerhalb eines Pakets).

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
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Gibt eine CRC-Prüfsumme (Cyclic Redundancy Check) der[`Data`](./data/) Inhalt. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Ruft die Zeichenfolge ab oder legt sie fest, die diesen benutzerdefinierten XML-Teil in einem OOXML-Dokument identifiziert. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Gibt den Satz von XML-Schemas an, die diesem benutzerdefinierten XML-Teil zugeordnet sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Erstellt eine ausreichend tiefe Kopie des Objekts. Dupliziert die Bytes der nicht[`Data`](./data/) wert. |

### Bemerkungen

Ein DOCX- oder DOC-Dokument kann einen oder mehrere benutzerdefinierte XML-Datenspeicherteile enthalten. Aspose.Words bewahrt und ermöglicht das Erstellen und Extrahieren von benutzerdefinierten XML-Daten über die[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) Sammlung.

### Beispiele

Zeigt, wie ein strukturiertes Dokument-Tag mit benutzerdefinierten XML-Daten erstellt wird.

```csharp
Document doc = new Document();

// Erstellen Sie einen XML-Teil, der Daten enthält, und fügen Sie ihn der Sammlung des Dokuments hinzu.
// Wenn wir die Registerkarte "Entwickler" in Microsoft Word aktivieren,
// Wir können Elemente aus dieser Sammlung zusammen mit einigen Standardelementen im "XML Mapping Pane" finden.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Im Folgenden finden Sie zwei Möglichkeiten, auf XML-Teile zu verweisen.
// 1 - Durch einen Index in der benutzerdefinierten XML-Teilsammlung:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Nach GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Eine XML-Schemazuordnung hinzufügen.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Klonen Sie einen Teil und fügen Sie ihn dann in die Sammlung ein.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Iteriere durch die Sammlung und drucke den Inhalt jedes Teils.
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

// Verwenden Sie die Methode "RemoveAt", um den geklonten Teil nach Index zu entfernen.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Klonen Sie die XML-Teilesammlung und verwenden Sie dann die "Clear"-Methode, um alle ihre Elemente auf einmal zu entfernen.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Erstellen Sie ein strukturiertes Dokument-Tag, das den Inhalt unseres Teils anzeigt, und fügen Sie es in den Dokumentkörper ein.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)


