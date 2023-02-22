---
title: StructuredDocumentTagRangeStart.XmlMapping
second_title: Aspose.Words för .NET API Referens
description: StructuredDocumentTagRangeStart fast egendom. Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttaggintervall till XML data i en anpassad XMLdel av det aktuella dokumentet.
type: docs
weight: 180
url: /sv/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Hämtar ett objekt som representerar mappningen av detta strukturerade dokumenttaggintervall till XML data i en anpassad XML-del av det aktuella dokumentet.

```csharp
public XmlMapping XmlMapping { get; }
```

### Anmärkningar

Du kan använda[`SetMapping`](../../xmlmapping/setmapping/) metod för detta objekt för att mappa ett strukturerat dokumenttaggområde till XML-data.

### Exempel

Visar hur man ställer in XML-mappningar för intervallstarten för en strukturerad dokumenttagg.

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
// det kommer bara att visa en del av CustomXmlPart som XPath pekar på.
// Denna XPath kommer att peka på innehållets andra "<text>" element i den första "<root>" element i vår CustomXmlPart.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Se även

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* namnutrymme [Aspose.Words.Markup](../../structureddocumenttagrangestart/)
* hopsättning [Aspose.Words](../../../)


