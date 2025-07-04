---
title: Document.RevisionsView
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words for .NET
description: Effortlessly manage document revisions! Choose between original or updated versions for seamless collaboration and enhanced productivity.
type: docs
weight: 380
url: /net/aspose.words/document/revisionsview/
---
## Document.RevisionsView property

Gets or sets a value indicating whether to work with the original or revised version of a document.

```csharp
public RevisionsView RevisionsView { get; set; }
```

## Remarks

The default value is .

## Examples

Shows how to switch between the revised and the original view of a document.

```csharp
Document doc = new Document(MyDir + "Revisions at list levels.docx");
doc.UpdateListLabels();

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;
Assert.That(paragraphs[0].ListLabel.LabelString, Is.EqualTo("1."));
Assert.That(paragraphs[1].ListLabel.LabelString, Is.EqualTo("a."));
Assert.That(paragraphs[2].ListLabel.LabelString, Is.EqualTo(string.Empty));

// View the document object as if all the revisions are accepted. Currently supports list labels.
doc.RevisionsView = RevisionsView.Final;

Assert.That(paragraphs[0].ListLabel.LabelString, Is.EqualTo(string.Empty));
Assert.That(paragraphs[1].ListLabel.LabelString, Is.EqualTo("1."));
Assert.That(paragraphs[2].ListLabel.LabelString, Is.EqualTo("a."));
```

### See Also

* enum [RevisionsView](../../revisionsview/)
* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
