---
title: PageSetup.chapterPageSeparator property
linktitle: chapterPageSeparator property
articleTitle: chapterPageSeparator property
second_title: Aspose.Words for NodeJs
description: "PageSetup.chapterPageSeparator property. Gets or sets the separator character that appears between the chapter number and the page number."
type: docs
weight: 90
url: /nodejs-net/aspose.words/pagesetup/chapterPageSeparator/
---

## PageSetup.chapterPageSeparator property

Gets or sets the separator character that appears between the chapter number and the page number.


```js
get chapterPageSeparator(): Aspose.Words.ChapterPageSeparator
```

### Remarks

Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.




### Examples

Shows how to work with page chapters.

```js
let doc = new aw.Document(base.myDir + "Big document.docx");

let pageSetup = doc.firstSection.pageSetup;

pageSetup.pageNumberStyle = aw.NumberStyle.UppercaseRoman;
pageSetup.chapterPageSeparator = aw.ChapterPageSeparator.Colon;
pageSetup.headingLevelForChapter = 1;
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

