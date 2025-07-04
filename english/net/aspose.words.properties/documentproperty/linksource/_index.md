---
title: DocumentProperty.LinkSource
linktitle: LinkSource
articleTitle: LinkSource
second_title: Aspose.Words for .NET
description: Discover the LinkSource property for DocumentProperty, effortlessly access the source of your linked custom document properties for enhanced document management.
type: docs
weight: 20
url: /net/aspose.words.properties/documentproperty/linksource/
---
## DocumentProperty.LinkSource property

Gets the source of a linked custom document property.

```csharp
public string LinkSource { get; }
```

## Examples

Shows how to link a custom document property to a bookmark.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("MyBookmark");
builder.Write("Hello world!");
builder.EndBookmark("MyBookmark");

// Link a new custom property to a bookmark. The value of this property
// will be the contents of the bookmark that it references in the "LinkSource" member.
CustomDocumentProperties customProperties = doc.CustomDocumentProperties;
DocumentProperty customProperty = customProperties.AddLinkToContent("Bookmark", "MyBookmark");

Assert.That(customProperty.IsLinkToContent, Is.EqualTo(true));
Assert.That(customProperty.LinkSource, Is.EqualTo("MyBookmark"));
Assert.That(customProperty.Value, Is.EqualTo("Hello world!"));

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### See Also

* class [DocumentProperty](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
