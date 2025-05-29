---
title: CustomXmlPart Class
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Markup.CustomXmlPart för effektiv hantering av anpassad XML-datalagring i paket. Förbättra din dokumenthantering idag!
type: docs
weight: 4610
url: /sv/net/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class

Representerar en anpassad XML-datalagringsdel (anpassade XML-data i ett paket).

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
| [Data](../../aspose.words.markup/customxmlpart/data/) { get; set; } | Hämtar eller ställer in XML-innehållet i denna anpassade XML-datalagringsdel. |
| [DataChecksum](../../aspose.words.markup/customxmlpart/datachecksum/) { get; } | Anger en cyklisk redundanskontroll (CRC) för[`Data`](./data/) innehåll. |
| [Id](../../aspose.words.markup/customxmlpart/id/) { get; set; } | Hämtar eller ställer in strängen som identifierar denna anpassade XML-del i ett OOXML-dokument. |
| [Schemas](../../aspose.words.markup/customxmlpart/schemas/) { get; } | Anger den uppsättning XML-scheman som är associerade med denna anpassade XML-del. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.markup/customxmlpart/clone/)() | Skapar en "tillräckligt djup" kopia av objektet. Duplicerar inte byten för[`Data`](./data/) värde. |

## Anmärkningar

Ett DOCX- eller DOC-dokument kan innehålla en eller flera delar av anpassad XML-datalagring. Aspose.Words bevarar och tillåter att skapa och extrahera anpassad XML-data via[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) samling.

## Exempel

Visar hur man skapar en strukturerad dokumenttagg med anpassad XML-data.

```csharp
Document doc = new Document();

// Konstruera en XML-del som innehåller data och lägg till den i dokumentets samling.
// Om vi aktiverar fliken "Utvecklare" i Microsoft Word,
// vi kan hitta element från den här samlingen i "XML-mappningsrutan", tillsammans med några standardelement.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Nedan följer två sätt att referera till XML-delar.
// 1 - Av ett index i den anpassade XML-delsamlingen:
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

// Använd metoden "RemoveAt" för att ta bort den klonade delen via index.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Klona XML-delsamlingen och använd sedan "Rensa"-metoden för att ta bort alla dess element på en gång.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Skapa en strukturerad dokumenttagg som visar innehållet i vår del och infogar den i dokumentets brödtext.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Se även

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
