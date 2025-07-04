---
title: CustomDocumentProperties.AddLinkToContent
linktitle: AddLinkToContent
articleTitle: AddLinkToContent
second_title: Aspose.Words for .NET
description: Discover the CustomDocumentProperties AddLinkToContent method to effortlessly create linked custom document properties for enhanced document management.
type: docs
weight: 20
url: /net/aspose.words.properties/customdocumentproperties/addlinktocontent/
---
## CustomDocumentProperties.AddLinkToContent method

Creates a new linked to content custom document property.

```csharp
public DocumentProperty AddLinkToContent(string name, string linkSource)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the property. |
| linkSource | String | The source of the property. |

### Return Value

The newly created property object or `null` when the *linkSource* is invalid.

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
