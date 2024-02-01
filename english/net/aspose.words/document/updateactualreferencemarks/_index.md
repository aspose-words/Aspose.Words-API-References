---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words for .NET
description: Document UpdateActualReferenceMarks method. Updates the ActualReferenceMark property of all footnotes and endnotes in the document in C#.
type: docs
weight: 780
url: /net/aspose.words/document/updateactualreferencemarks/
---
## Document.UpdateActualReferenceMarks method

Updates the [`ActualReferenceMark`](../../../aspose.words.notes/footnote/actualreferencemark/) property of all footnotes and endnotes in the document.

```csharp
public void UpdateActualReferenceMarks()
```

## Remarks

Updating fields ([`UpdateFields`](../updatefields/)) may be necessary to get the correct result.

## Examples

Shows how to get actual footnote reference mark.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

Footnote footnote = (Footnote)doc.GetChild(NodeType.Footnote, 1, true);
doc.UpdateFields();
doc.UpdateActualReferenceMarks();

Assert.AreEqual("1", footnote.ActualReferenceMark);
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
