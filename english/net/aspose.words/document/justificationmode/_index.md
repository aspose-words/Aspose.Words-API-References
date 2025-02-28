---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words for .NET
description: Discover how to optimize your document's character spacing with the JustificationMode property. Enhance readability and improve presentation effortlessly!
type: docs
weight: 240
url: /net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Gets or sets the character spacing adjustment of a document.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Examples

Shows how to manage character spacing control.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### See Also

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
