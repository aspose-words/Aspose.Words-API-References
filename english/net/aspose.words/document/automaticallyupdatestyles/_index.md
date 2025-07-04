---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words for .NET
description: Discover how the AutomaticallyUpdateStyles property in MS Word ensures your document's styles sync with the template every time you open it, enhancing consistency.
type: docs
weight: 30
url: /net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Gets or sets a flag indicating whether the styles in the document are updated to match the styles in the attached template each time the document is opened in MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Examples

Shows how to attach a template to a document.

```csharp
Document doc = new Document();

// Microsoft Word documents by default come with an attached template called "Normal.dotm".
// There is no default template for blank Aspose.Words documents.
Assert.That(doc.AttachedTemplate, Is.EqualTo(string.Empty));

// Attach a template, then set the flag to apply style changes
// within the template to styles in our document.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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
