---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words for .NET
description: DocumentBase Document property. Gets this instance in C#.
type: docs
weight: 20
url: /net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

Gets this instance.

```csharp
public override DocumentBase Document { get; }
```

## Examples

Shows how to create simple document.

```csharp
Document doc = new Document();

// New Document objects by default come with the minimal set of nodes
// required to begin adding content such as text and shapes: a Section, a Body, and a Paragraph.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### See Also

* class [DocumentBase](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
