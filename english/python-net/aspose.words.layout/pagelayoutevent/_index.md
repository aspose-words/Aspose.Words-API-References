---
title: PageLayoutEvent enumeration
linktitle: PageLayoutEvent enumeration
articleTitle: PageLayoutEvent enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.PageLayoutEvent enumeration. A code of event raised during page layout model build and rendering."
type: docs
weight: 90
url: /python-net/aspose.words.layout/pagelayoutevent/
---

## PageLayoutEvent enumeration

A code of event raised during page layout model build and rendering.



Page layout model is built in two steps.
First, "conversion step", this is when page layout pulls document content and creates object graph.
Second, "reflow step", this is when structures are split, merged and arranged into pages.



Depending of the operation which triggered build, page layout model may or may not be further rendered into fixed page format.
For example, computing number of pages in the document or updating fields does not require rendering, whereas export to Pdf does.




### Members

| Name | Description |
| --- | --- |
| NONE | Default value |
| WATCH_DOG | Corresponds to a checkpoint in code which is often visited and which is suitable to abort process. |
| BUILD_STARTED | Build of the page layout has started. Fired once. This is the first event which occurs when [Document.update_page_layout()](../../aspose.words/document/update_page_layout/#default) is called. |
| BUILD_FINISHED | Build of the page layout has finished. Fired once. This is the last event which occurs when [Document.update_page_layout()](../../aspose.words/document/update_page_layout/#default) is called. |
| CONVERSION_STARTED | Conversion of document model to page layout has started. Fired once. This occurs when layout model starts pulling document content. |
| CONVERSION_FINISHED | Conversion of document model to page layout has finished. Fired once. This occurs when layout model stops pulling document content. |
| REFLOW_STARTED | Reflow of the page layout has started. Fired once. This occurs when layout model starts reflowing document content. |
| REFLOW_FINISHED | Reflow of the page layout has finished. Fired once. This occurs when layout model stops reflowing document content. |
| PART_REFLOW_STARTED | Reflow of the page has started. Note that page may reflow multiple times and that reflow may restart before it is finished. |
| PART_REFLOW_FINISHED | Reflow of the page has finished. Note that page may reflow multiple times and that reflow may restart before it is finished. |
| PART_RENDERING_STARTED | Rendering of page has started. This is fired once per page. |
| PART_RENDERING_FINISHED | Rendering of page has finished. This is fired once per page. |

### See Also

* module [aspose.words.layout](../)

