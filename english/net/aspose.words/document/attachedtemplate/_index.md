---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words for .NET
description: Discover how to manage your Document AttachedTemplate property efficiently. Easily set or retrieve the full path of your document's template for seamless integration.
type: docs
weight: 20
url: /net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Gets or sets the full path of the template attached to the document.

```csharp
public string AttachedTemplate { get; set; }
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Throws if you attempt to set to a `null` value. |

## Remarks

Empty string means the document is attached to the Normal template.

## Examples

Shows how to set a default template for documents that do not have attached templates.

```csharp
Document doc = new Document();

// Enable automatic style updating, but do not attach a template document.
doc.AutomaticallyUpdateStyles = true;

Assert.That(doc.AttachedTemplate, Is.EqualTo(string.Empty));

// Since there is no template document, the document had nowhere to track style changes.
// Use a SaveOptions object to automatically set a template
// if a document that we are saving does not have one.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
