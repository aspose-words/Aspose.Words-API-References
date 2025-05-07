---
title: Paragraph.joinRunsWithSameFormatting method
linktitle: joinRunsWithSameFormatting method
articleTitle: joinRunsWithSameFormatting method
second_title: Aspose.Words for Node.js
description: "Paragraph.joinRunsWithSameFormatting method. Joins runs with the same formatting in the paragraph."
type: docs
weight: 270
url: /nodejs-net/aspose.words/paragraph/joinRunsWithSameFormatting/
---

## joinRunsWithSameFormatting() {#default}

Joins runs with the same formatting in the paragraph.


```js
joinRunsWithSameFormatting()
```

### Returns

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.


### Examples

Shows how to simplify paragraphs by merging superfluous runs.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert four runs of text into the paragraph.
builder.write("Run 1. ");
builder.write("Run 2. ");
builder.write("Run 3. ");
builder.write("Run 4. ");

// If we open this document in Microsoft Word, the paragraph will look like one seamless text body.
// However, it will consist of four separate runs with the same formatting. Fragmented paragraphs like this
// may occur when we manually edit parts of one paragraph many times in Microsoft Word.
let para = builder.currentParagraph;

expect(para.runs.count).toEqual(4);

// Change the style of the last run to set it apart from the first three.
para.runs.at(3).font.styleIdentifier = aw.StyleIdentifier.Emphasis;

// We can run the "JoinRunsWithSameFormatting" method to optimize the document's contents
// by merging similar runs into one, reducing their overall count.
// This method also returns the number of runs that this method merged.
// These two merges occurred to combine Runs #1, #2, and #3,
// while leaving out Run #4 because it has an incompatible style.
expect(para.joinRunsWithSameFormatting()).toEqual(2);

// The number of runs left will equal the original count
// minus the number of run merges that the "JoinRunsWithSameFormatting" method carried out.
expect(para.runs.count).toEqual(2);
expect(para.runs.at(0).text).toEqual("Run 1. Run 2. Run 3. ");
expect(para.runs.at(1).text).toEqual("Run 4. ");
```

### See Also

* module [Aspose.Words](../../)
* class [Paragraph](../)

