---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words for .NET
description: Discover the BuiltInDocumentProperties HyperlinkBase property to optimize relative hyperlinks in your documents for seamless navigation and enhanced user experience.
type: docs
weight: 120
url: /net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Specifies the base string used for evaluating relative hyperlinks in this document.

```csharp
public string HyperlinkBase { get; set; }
```

## Remarks

Aspose.Words does not use this property.

## Examples

Shows how to store the base part of a hyperlink in the document's properties.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a relative hyperlink to a document in the local file system named "Document.docx".
// Clicking on the link in Microsoft Word will open the designated document, if it is available.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// This link is relative. If there is no "Document.docx" in the same folder
// as the document that contains this link, the link will be broken.
Assert.That(File.Exists(ArtifactsDir + "Document.docx"), Is.False);
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// The document we are trying to link to is in a different directory to the one we are planning to save the document in.
// We could fix links like this by putting an absolute filename in each one. 
// Alternatively, we could provide a base link that every hyperlink with a relative filename
// will prepend to its link when we click on it. 
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.That(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address), Is.True);

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### See Also

* class [BuiltInDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
