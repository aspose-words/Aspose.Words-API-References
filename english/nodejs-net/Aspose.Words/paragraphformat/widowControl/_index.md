---
title: ParagraphFormat.widowControl property
linktitle: widowControl property
articleTitle: widowControl property
second_title: Aspose.Words for Node.js
description: "ParagraphFormat.widowControl property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /nodejs-net/aspose.words/paragraphformat/widowControl/
---

## ParagraphFormat.widowControl property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```js
get widowControl(): boolean
```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// When we write the text that does not fit onto one page, one line may spill over onto the next page.
// The single line that ends up on the next page is called an "Orphan",
// and the previous line where the orphan broke off is called a "Widow".
// We can fix orphans and widows by rearranging text via font size, spacing, or page margins.
// If we wish to preserve our document's dimensions, we can set this flag to "true"
// to push widows onto the same page as their respective orphans. 
// Leave this flag as "false" will leave widow/orphan pairs in text.
// Every paragraph has this setting accessible in Microsoft Word via Home -> Paragraph -> Paragraph Settings
// (button on bottom right hand corner of "Paragraph" tab) -> "Widow/Orphan control".
builder.paragraphFormat.widowControl = widowControl; 

// Insert text that produces an orphan and a widow.
builder.font.size = 68;
builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.save(base.artifactsDir + "ParagraphFormat.widowControl.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [ParagraphFormat](../)

