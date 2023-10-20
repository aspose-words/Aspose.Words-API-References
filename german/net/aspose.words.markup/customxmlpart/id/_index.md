---
title: CustomXmlPart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words für .NET
description: CustomXmlPart Id eigendom. Ruft die Zeichenfolge ab die diesen benutzerdefinierten XMLTeil in einem OOXMLDokument identifiziert oder legt diese fest in C#.
type: docs
weight: 40
url: /de/net/aspose.words.markup/customxmlpart/id/
---
## CustomXmlPart.Id property

Ruft die Zeichenfolge ab, die diesen benutzerdefinierten XML-Teil in einem OOXML-Dokument identifiziert, oder legt diese fest.

```csharp
public string Id { get; set; }
```

## Bemerkungen

ISO/IEC 29500 gibt an, dass dieser Wert eine GUID ist, aber alte Versionen von Microsoft Word erlaubten hier eine beliebige -Zeichenfolge. Aspose.Words macht dasselbe für das ECMA-376-Format. Beachten Sie jedoch, dass Microsoft Word Online ein Dokument, das mit einem Nicht-GUID-Wert erstellt wurde, nicht öffnen kann. Daher ist eine GUID der bevorzugte Wert für diese Eigenschaft.

Ein gültiger Wert muss ein Bezeichner sein, der unter allen benutzerdefinierten XML-Datenteilen in diesem Dokument eindeutig ist.

Der Standardwert ist eine leere Zeichenfolge. Der Wert kann nicht sein`Null`.

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

* class [CustomXmlPart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
