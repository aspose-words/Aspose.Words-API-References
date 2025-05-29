---
title: XmlMapping.PrefixMappings
linktitle: PrefixMappings
articleTitle: PrefixMappings
second_title: Aspose.Words för .NET
description: Upptäck egenskapen XmlMapping PrefixMappings för sömlös mappning av XML-namnrymdsprefix och effektiv XPath-utvärdering. Förbättra din XML-bearbetning idag!
type: docs
weight: 30
url: /sv/net/aspose.words.markup/xmlmapping/prefixmappings/
---
## XmlMapping.PrefixMappings property

Returnerar XML-namnrymdsprefixmappningar för att utvärdera[`XPath`](../xpath/) .

```csharp
public string PrefixMappings { get; }
```

## Anmärkningar

Anger den uppsättning prefixmappningar som ska användas för att tolka XPath-uttrycket när XPath-uttrycket utvärderas mot de anpassade XML-datadelarna i dokumentet.

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

* class [XmlMapping](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
