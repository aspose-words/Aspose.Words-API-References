---
title: BuiltInDocumentProperties.ScaleCrop
linktitle: ScaleCrop
articleTitle: ScaleCrop
second_title: Aspose.Words for .NET
description: Discover the ScaleCrop property in BuiltInDocumentProperties, which controls thumbnail display—ensuring optimal viewing with cropped or scaled images.
type: docs
weight: 260
url: /net/aspose.words.properties/builtindocumentproperties/scalecrop/
---
## BuiltInDocumentProperties.ScaleCrop property

Indicates whether document thumbnail is cropped or scaled to fit the display.

```csharp
public bool ScaleCrop { get; }
```

## Remarks

Aspose.Words does not update this property.

## Examples

Shows how to get extended properties.

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### See Also

* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
