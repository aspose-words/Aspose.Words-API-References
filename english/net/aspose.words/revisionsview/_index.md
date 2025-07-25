---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.RevisionsView enum to easily choose between original and revised document versions for streamlined editing and collaboration.
type: docs
weight: 5540
url: /net/aspose.words/revisionsview/
---
## RevisionsView enumeration

Allows to specify whether to work with the original or revised version of a document.

```csharp
public enum RevisionsView
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Original | `0` | Specifies original version of a document. |
| Final | `1` | Specifies revised version of a document. |

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

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
