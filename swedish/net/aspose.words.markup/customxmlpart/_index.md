---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words för .NET
description: Aspose.Words.Markup.CustomXmlPart klass. Representerar en anpassad XMLdatalagringsdel anpassad XMLdata i ett paket i C#.
type: docs
weight: 3920
url: /sv/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Representerar en anpassad XML-datalagringsdel (anpassad XML-data i ett paket).

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class CustomXmlPart
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CustomXmlPart](customxmlpart/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Hämtar eller ställer in XML-innehållet för denna anpassade XML-datalagringsdel. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Anger en cyklisk redundanskontroll (CRC) checksumma för[`Data`](./data/) innehåll. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Hämtar eller ställer in strängen som identifierar denna anpassade XML-del i ett OOXML-dokument. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Anger uppsättningen XML-scheman som är associerade med den här anpassade XML-delen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Gör en "tillräckligt djup" kopia av objektet. Duplicerar inte byten för[`Data`](./data/) värde. |

## Anmärkningar

Ett DOCX- eller DOC-dokument kan innehålla en eller flera Custom XML Data Storage-delar. Aspose.Words bevarar och gör det möjligt att skapa och extrahera anpassade XML-data via[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) samling.

## Exempel

Visar hur man skapar en strukturerad dokumenttagg med anpassade XML-data.

```csharp
Document doc = new Document();

// Konstruera en XML-del som innehåller data och lägg till den i dokumentets samling.
// Om vi aktiverar fliken "Utvecklare" i Microsoft Word,
// vi kan hitta element från denna samling i "XML Mapping Pane", tillsammans med några standardelement.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Nedan finns två sätt att referera till XML-delar.
// 1 - Genom ett index i den anpassade XML-delsamlingen:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Av GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Lägg till en XML-schemaassociation.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Klona en del och infoga den sedan i samlingen.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Iterera genom samlingen och skriv ut innehållet i varje del.
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

// Använd metoden "RemoveAt" för att ta bort den klonade delen efter index.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Klona XML-delsamlingen och använd sedan metoden "Rensa" för att ta bort alla dess element på en gång.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Skapa en strukturerad dokumenttagg som visar vår dels innehåll och infoga den i dokumentets brödtext.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Se även

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
