﻿---
title: LayoutOptions class
linktitle: LayoutOptions class
articleTitle: LayoutOptions class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Layout.LayoutOptions class. Holds the options that allow controlling the document layout process"
type: docs
weight: 70
url: /nodejs-net/aspose.words.layout/layoutoptions/
---

## LayoutOptions class

Holds the options that allow controlling the document layout process.
To learn more, visit the [Converting to Fixed-page Format](https://docs.aspose.com/words/nodejs-net/converting-to-fixed-page-format/) documentation article.




### Remarks

You do not create instances of this class directly. Use the [Document.layoutOptions](../../aspose.words/document/layoutOptions/) property to access layout options for this document.


Note that after changing any of the options present in this class, [Document.updatePageLayout()](../../aspose.words/document/updatePageLayout/#default) method
should be called in order for the changed options to be applied to the layout.




### Constructors
| Name | Description |
| --- | --- |
| [LayoutOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [callback](./callback/) | Gets or sets [IPageLayoutCallback](../ipagelayoutcallback/) implementation used by page layout model. |
| [commentDisplayMode](./commentDisplayMode/) | Gets or sets the way comments are rendered. Default value is [CommentDisplayMode.ShowInBalloons](../commentdisplaymode/#ShowInBalloons). |
| [continuousSectionPageNumberingRestart](./continuousSectionPageNumberingRestart/) | Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering. |
| [ignorePrinterMetrics](./ignorePrinterMetrics/) | Gets or sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored. Default is ``true``. |
| [keepOriginalFontMetrics](./keepOriginalFontMetrics/) | Gets or sets an indication of whether the original font metrics should be used after font substitution. Default is ``true``. |
| [revisionOptions](./revisionOptions/) | Gets revision options. |
| [showHiddenText](./showHiddenText/) | Gets or sets indication of whether hidden text in the document is rendered. Default is ``false``. |
| [showParagraphMarks](./showParagraphMarks/) | Gets or sets indication of whether paragraph marks are rendered. Default is ``false``. |

### See Also

* module [Aspose.Words.Layout](../)

