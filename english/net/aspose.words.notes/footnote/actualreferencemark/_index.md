---
title: Footnote.ActualReferenceMark
linktitle: ActualReferenceMark
articleTitle: ActualReferenceMark
second_title: Aspose.Words for .NET
description: Footnote ActualReferenceMark property. Gets the actual text of the reference mark displayed in the document for this footnote in C#.
type: docs
weight: 20
url: /net/aspose.words.notes/footnote/actualreferencemark/
---
## Footnote.ActualReferenceMark property

Gets the actual text of the reference mark displayed in the document for this footnote.

```csharp
public string ActualReferenceMark { get; }
```

## Remarks

To initially populate values of this property for all reference marks of the document, or to update the values after changes in the document that might affect the reference marks, you must execute the [`UpdateActualReferenceMarks`](../../../aspose.words/document/updateactualreferencemarks/) method. Updating fields ([`UpdateFields`](../../../aspose.words/document/updatefields/)) may also be necessary to get the correct result.

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

* class [Footnote](../)
* namespace [Aspose.Words.Notes](../../../aspose.words.notes/)
* assembly [Aspose.Words](../../../)
