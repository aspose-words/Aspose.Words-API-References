---
title: Document.joinRunsWithSameFormatting method
linktitle: joinRunsWithSameFormatting method
articleTitle: joinRunsWithSameFormatting method
second_title: Aspose.Words for NodeJs
description: "Document.joinRunsWithSameFormatting method. Joins runs with same formatting in all paragraphs of the document."
type: docs
weight: 640
url: /nodejs-net/aspose.words/document/joinRunsWithSameFormatting/
---

## joinRunsWithSameFormatting() {#default}

Joins runs with same formatting in all paragraphs of the document.


```js
joinRunsWithSameFormatting()
```

### Remarks

This is an optimization method. Some documents contain adjacent runs with same formatting.
Usually this occurs if a document was intensively edited manually.
You can reduce the document size and speed up further processing by joining these runs.

The operation checks every [Paragraph](../../paragraph/) node in the document for adjacent [Run](../../run/)
nodes having identical properties. It ignores unique identifiers used to track editing sessions of run
creation and modification. First run in every joining sequence accumulates all text. Remaining
runs are deleted from the document.




### Returns

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.


### Examples

Shows how to join runs in a document to reduce unneeded runs.

```js
// Open a document that contains adjacent runs of text with identical formatting,
// which commonly occurs if we edit the same paragraph multiple times in Microsoft Word.
let doc = new aw.Document(base.myDir + "Rendering.docx");
// If any number of these runs are adjacent with identical formatting,
// then the document may be simplified.
expect(doc.getChildNodes(aw.NodeType.Run, true).count).toEqual(317);
// Combine such runs with this method and verify the number of run joins that will take place.
expect(doc.joinRunsWithSameFormatting()).toEqual(121);
// The number of joins and the number of runs we have after the join
// should add up the number of runs we had initially.
expect(doc.getChildNodes(aw.NodeType.Run, true).count).toEqual(196);
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

