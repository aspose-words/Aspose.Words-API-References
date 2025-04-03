---
title: PageSetup.headingLevelForChapter property
linktitle: headingLevelForChapter property
articleTitle: headingLevelForChapter property
second_title: Aspose.Words for NodeJs
description: "PageSetup.headingLevelForChapter property. Gets or sets the heading level style that is applied to the chapter titles in the document."
type: docs
weight: 180
url: /nodejs-net/aspose.words/pagesetup/headingLevelForChapter/
---

## PageSetup.headingLevelForChapter property

Gets or sets the heading level style that is applied to the chapter titles in the document.


```js
get headingLevelForChapter(): number
```

### Remarks

Can be a number from 0 through 9. 0 means no chapter number if applied to page number.

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

