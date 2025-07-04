---
title: BuiltInDocumentProperties.SharedDocument
linktitle: SharedDocument
articleTitle: SharedDocument
second_title: Aspose.Words for .NET
description: Discover the BuiltInDocumentProperties SharedDocument feature that reveals if your document is shared, enhancing collaboration and accessibility.
type: docs
weight: 280
url: /net/aspose.words.properties/builtindocumentproperties/shareddocument/
---
## BuiltInDocumentProperties.SharedDocument property

Indicates whether the document is a shared document.

```csharp
public bool SharedDocument { get; }
```

## Remarks

Aspose.Words does not update this property.

## Examples

Shows how to get extended properties.

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.That(doc.BuiltInDocumentProperties.ScaleCrop, Is.True);
Assert.That(doc.BuiltInDocumentProperties.SharedDocument, Is.True);
Assert.That(doc.BuiltInDocumentProperties.HyperlinksChanged, Is.True);
```

### See Also

* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
