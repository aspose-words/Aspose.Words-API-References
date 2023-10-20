---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words för .NET
description: CustomDocumentProperties AddLinkToContent metod. Skapar en ny länkad till innehåll anpassad dokumentegenskap i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Skapar en ny länkad till innehåll anpassad dokumentegenskap.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Namnet på fastigheten. |
| linkSource | String | Källan till fastigheten. |

### Returvärde

Det nyskapade egenskapsobjektet eller`null` när*linkSource* är ogiltig.

## Exempel

Visar hur man länkar en anpassad dokumentegenskap till ett bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Länka en ny anpassad egenskap till ett bokmärke. Värdet på denna fastighet
// kommer att vara innehållet i bokmärket som det refererar till i "LinkSource"-medlemmen.
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
