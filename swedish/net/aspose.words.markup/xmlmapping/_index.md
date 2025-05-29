---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Markup.XmlMapping för att sömlöst länka strukturerade dokumenttaggar med XML-element, vilket förbättrar dokumentets dataintegration.
type: docs
weight: 4790
url: /sv/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Anger informationen som används för att upprätta en mappning mellan den överordnade strukturerade dokumenttaggen och ett XML-element som lagras i en anpassad XML-datadel i dokumentet.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class XmlMapping
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Returnerar den anpassade XML-datadelen till vilken den överordnade strukturerade dokumenttaggen är mappad. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Returer`sann` om den överordnade strukturerade dokumenttaggen har mappats till XML-data. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Returnerar XML-namnrymdsprefixmappningar för att utvärdera[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Anger den anpassade XML-dataidentifieraren för den anpassade XML-datadelen som ska användas för att utvärdera[`XPath`](./xpath/) uttryck. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Returnerar XPath-uttrycket, vilket utvärderas för att hitta den anpassade XML-noden som är mappad till den överordnade taggen för strukturerat dokument. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Tar bort mappningen av det överordnade strukturerade dokumentet till XML-data. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Anger en mappning mellan den överordnade strukturerade dokumenttaggen och en XML-nod i en anpassad XML-datadel. |

## Exempel

Visar hur man ställer in XML-mappningar för anpassade XML-delar.

```csharp
Document doc = new Document();

// Konstruera en XML-del som innehåller text och lägg till den i dokumentets CustomXmlPart-samling.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Skapa en strukturerad dokumenttagg som visar innehållet i vår CustomXmlPart.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Ange en mappning för vår strukturerade dokumenttagg. Denna mappning kommer att instruera
// vår strukturerade dokumenttagg för att visa en del av XML-delens textinnehåll som XPath pekar på.
// I det här fallet kommer det att vara innehållet i det andra "<text>"-elementet i det första "<root>"-elementet: "Textelement #2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tagg.XmlMapping.PrefixMappings);

// Lägg till taggen "structured document" i dokumentet för att visa innehållet från vår anpassade del.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Se även

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
