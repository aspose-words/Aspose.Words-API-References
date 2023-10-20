---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words för .NET
description: DocumentProperty LinkSource fast egendom. Hämtar källan till en länkad anpassad dokumentegenskap i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Hämtar källan till en länkad anpassad dokumentegenskap.

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

* class [DocumentProperty](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
