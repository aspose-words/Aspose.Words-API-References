---
title: DocumentProperty.IsLinkToContent
linktitle: IsLinkToContent
articleTitle: IsLinkToContent
second_title: Aspose.Words for .NET
description: Discover if DocumentProperty's IsLinkToContent property connects to content. Enhance your workflow with seamless document management solutions.
type: docs
weight: 10
url: /net/aspose.words.properties/documentproperty/islinktocontent/
---
## DocumentProperty.IsLinkToContent property

Shows whether this property is linked to content or not.

```csharp
public bool IsLinkToContent { get; }
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
