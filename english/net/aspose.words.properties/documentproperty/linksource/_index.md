---
title: DocumentProperty.LinkSource
second_title: Aspose.Words for .NET API Reference
description: DocumentProperty property. Gets the source of a linked custom document property in C#.
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

Assert.AreEqual(true, customProperty.IsLinkToContent);
Assert.AreEqual("MyBookmark", customProperty.LinkSource);
Assert.AreEqual("Hello world!", customProperty.Value);

doc.Save(ArtifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### See Also

* class [DocumentProperty](../)
* namespace [Aspose.Words.Properties](../../documentproperty/)
* assembly [Aspose.Words](../../../)
