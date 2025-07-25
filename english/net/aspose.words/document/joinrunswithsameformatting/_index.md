---
title: Document.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words for .NET
description: Discover how the JoinRunsWithSameFormatting method seamlessly merges formatted text in your document's paragraphs for a polished, professional look.
type: docs
weight: 660
url: /net/aspose.words/document/joinrunswithsameformatting/
---
## Document.JoinRunsWithSameFormatting method

Joins runs with same formatting in all paragraphs of the document.

```csharp
public int JoinRunsWithSameFormatting()
```

### Return Value

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.

## Remarks

This is an optimization method. Some documents contain adjacent runs with same formatting. Usually this occurs if a document was intensively edited manually. You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [`Paragraph`](../../paragraph/) node in the document for adjacent [`Run`](../../run/) nodes having identical properties. It ignores unique identifiers used to track editing sessions of run creation and modification. First run in every joining sequence accumulates all text. Remaining runs are deleted from the document.

## Examples

Shows how to join runs in a document to reduce unneeded runs.

```csharp
// Open a document that contains adjacent runs of text with identical formatting,
// which commonly occurs if we edit the same paragraph multiple times in Microsoft Word.
Document doc = new Document(MyDir + "Rendering.docx");

// If any number of these runs are adjacent with identical formatting,
// then the document may be simplified.
Assert.That(doc.GetChildNodes(NodeType.Run, true).Count, Is.EqualTo(317));

// Combine such runs with this method and verify the number of run joins that will take place.
Assert.That(doc.JoinRunsWithSameFormatting(), Is.EqualTo(121));

// The number of joins and the number of runs we have after the join
// should add up the number of runs we had initially.
Assert.That(doc.GetChildNodes(NodeType.Run, true).Count, Is.EqualTo(196));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
