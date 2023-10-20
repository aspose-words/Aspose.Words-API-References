---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words för .NET
description: Aspose.Words.Markup.XmlMapping klass. Anger informationen som används för att upprätta en mappning mellan den strukturerade dokumenttaggen parent och ett XMLelement lagrat i en anpassad XMLdatadel i dokumentet i C#.
type: docs
weight: 4100
url: /sv/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Anger informationen som används för att upprätta en mappning mellan den strukturerade dokumenttaggen parent och ett XML-element lagrat i en anpassad XML-datadel i dokumentet.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class XmlMapping
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Returnerar den anpassade XML-datadelen till vilken den överordnade strukturerade dokumenttaggen är mappad. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Returnerar`Sann` om den överordnade strukturerade dokumenttaggen har mappats till XML-data. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Returnerar XML-namnområdesprefixmappningar för att utvärdera[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Anger den anpassade XML-dataidentifieraren för den anpassade XML-datadelen som ska användas för att utvärdera[`XPath`](./xpath/) expression. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Returnerar XPath-uttrycket, som utvärderas för att hitta den anpassade XML-noden som är mappad till den överordnade strukturerade dokumenttaggen. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Tar bort mappningen av det överordnade strukturerade dokumentet till XML-data. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Ställer in en mappning mellan den överordnade strukturerade dokumenttaggen och en XML-nod för en anpassad XML-datadel. |

## Exempel

Visar hur du ställer in XML-mappningar för anpassade XML-delar.

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

// Ställ in en mappning för vår strukturerade dokumenttagg. Denna mappning kommer att instruera
// vår strukturerade dokumenttagg för att visa en del av XML-delens textinnehåll som XPath pekar på.
// I det här fallet kommer det att vara innehållet i den andra "<text>" element i den första "<root>" element: "Textelement #2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// Lägg till den strukturerade dokumenttaggen i dokumentet för att visa innehållet från vår anpassade del.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Se även

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
