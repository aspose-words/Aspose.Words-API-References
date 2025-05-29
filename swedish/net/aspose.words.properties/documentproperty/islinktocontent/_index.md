---
title: DocumentProperty.IsLinkToContent
linktitle: IsLinkToContent
articleTitle: IsLinkToContent
second_title: Aspose.Words för .NET
description: Upptäck om DocumentPropertys IsLinkToContent-egenskap kopplar till innehåll. Förbättra ditt arbetsflöde med sömlösa dokumenthanteringslösningar.
type: docs
weight: 10
url: /sv/net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

Visar om den här egenskapen är länkad till innehåll eller inte.

```csharp
public bool IsLinkToContent { get; }
```

## Exempel

Visar hur man länkar en anpassad dokumentegenskap till ett bokmärke.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Länka en ny anpassad egenskap till ett bokmärke. Värdet för denna egenskap
// kommer att vara innehållet i bokmärket som den refererar till i "LinkSource"-medlemmen.
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### Se även

* class [DocumentProperty](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
