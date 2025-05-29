---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen StructuredDocumentTagRangeStart XmlMapping kopplar ditt dokuments taggintervall till anpassade XML-data, vilket förbättrar dokumentintegrationen.
type: docs
weight: 190
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttaggintervall till XML-data i en anpassad XML-del av det aktuella dokumentet.

```csharp
public XmlMapping XmlMapping { get; }
```

## Anmärkningar

Du kan använda[`SetMapping`](../../xmlmapping/setmapping/) Metod för this -objektet för att mappa ett strukturerat dokumenttaggintervall till XML-data.

## Exempel

Visar hur man ställer in XML-mappningar för intervallets början av en strukturerad dokumenttagg.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// Konstruera en XML-del som innehåller text och lägg till den i dokumentets CustomXmlPart-samling.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Skapa en strukturerad dokumenttagg som visar innehållet i vår CustomXmlPart i dokumentet.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Om vi ställer in en mappning för vår strukturerade dokumenttagg,
// den kommer bara att visa en del av CustomXmlPart som XPath pekar på.
// Denna XPath kommer att peka på innehållets andra "<text>"-element i det första "<root>"-elementet i vår CustomXmlPart.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Se även

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
