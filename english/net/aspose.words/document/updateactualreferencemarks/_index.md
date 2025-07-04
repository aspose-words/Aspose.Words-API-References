---
title: Document.UpdateActualReferenceMarks
linktitle: UpdateActualReferenceMarks
articleTitle: UpdateActualReferenceMarks
second_title: Aspose.Words for .NET
description: Effortlessly update all footnotes and endnotes in your document with the Document UpdateActualReferenceMarks method, enhancing accuracy and efficiency.
type: docs
weight: 800
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

Assert.That(footnote.ActualReferenceMark, Is.EqualTo("1"));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
