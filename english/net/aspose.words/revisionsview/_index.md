---
title: RevisionsView Enum
linktitle: RevisionsView
articleTitle: RevisionsView
second_title: Aspose.Words for .NET
description: Aspose.Words.RevisionsView enum. Allows to specify whether to work with the original or revised version of a document in C#.
type: docs
weight: 4810
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
Assert.AreEqual("1.", paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual(string.Empty, paragraphs[2].ListLabel.LabelString);

// View the document object as if all the revisions are accepted. Currently supports list labels.
doc.RevisionsView = RevisionsView.Final;

Assert.AreEqual(string.Empty, paragraphs[0].ListLabel.LabelString);
Assert.AreEqual("1.", paragraphs[1].ListLabel.LabelString);
Assert.AreEqual("a.", paragraphs[2].ListLabel.LabelString);
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
