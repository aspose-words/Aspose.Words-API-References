---
title: XmlMapping.CustomXmlPart
linktitle: CustomXmlPart
articleTitle: CustomXmlPart
second_title: Aspose.Words för .NET
description: XmlMapping CustomXmlPart fast egendom. Returnerar den anpassade XMLdatadelen till vilken den överordnade strukturerade dokumenttaggen är mappad i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.markup/xmlmapping/customxmlpart/
---
## XmlMapping.CustomXmlPart property

Returnerar den anpassade XML-datadelen till vilken den överordnade strukturerade dokumenttaggen är mappad.

```csharp
public CustomXmlPart CustomXmlPart { get; }
```

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

* class [CustomXmlPart](../../customxmlpart/)
* class [XmlMapping](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
