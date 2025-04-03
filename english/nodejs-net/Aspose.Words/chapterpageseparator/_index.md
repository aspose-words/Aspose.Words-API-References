---
title: ChapterPageSeparator enumeration
linktitle: ChapterPageSeparator enumeration
articleTitle: ChapterPageSeparator enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.ChapterPageSeparator enumeration. Defines the separator character that appears between the chapter and page number."
type: docs
weight: 160
url: /nodejs-net/aspose.words/chapterpageseparator/
---

## ChapterPageSeparator enumeration

Defines the separator character that appears between the chapter and page number.


### Members

| Name | Description |
| --- | --- |
| Hyphen | A colon. |
| Period | A period. |
| Colon | A colon. |
| EmDash | An emphasized dash. |
| EnDash | A standard dash. |

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

* module [Aspose.Words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.chapterPageSeparator](../pagesetup/chapterPageSeparator/)

