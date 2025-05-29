---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LinkSource för DocumentProperty och få enkel åtkomst till källan för dina länkade anpassade dokumentegenskaper för förbättrad dokumenthantering.
type: docs
weight: 20
url: /sv/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Hämtar källan för en länkad anpassad dokumentegenskap.

```csharp
public string LinkSource { get; }
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
