---
title: IPageLayoutCallback class
linktitle: IPageLayoutCallback class
articleTitle: IPageLayoutCallback class
second_title: Aspose.Words for Python
description: "aspose.words.layout.IPageLayoutCallback class. Implement this interface if you want to have your own custom method called during build and rendering of page layout model."
type: docs
weight: 30
url: /python-net/aspose.words.layout/ipagelayoutcallback/
---

## IPageLayoutCallback class

Implement this interface if you want to have your own custom method called during build and rendering of page layout model.


### Remarks

The primary use for this interface is to allow application code to abort build process.


It is possible to build page layout model for only a few pages at start of the document then abort process and render only what has been built already.


Note, however, that rendering results may not match what would be rendered for each page if process would have finished.


This technique may not work for every document or may fail completely.




### Methods

| Name | Description |
| --- | --- |
|[ notify(args)](./notify/#pagelayoutcallbackargs) | This is called to notify of layout build and rendering progress. |

### Examples

Shows how to track layout changes with a layout callback (RenderPageLayoutCallback).

```python
class RenderPageLayoutCallback(aw.layout.IPageLayoutCallback):

    def __init__(self):
        self.m_num = None

    def notify(self, a):
        switch_condition = a.event
        if switch_condition == aw.layout.PageLayoutEvent.PART_REFLOW_FINISHED:
            self._notify_part_finished(a)
        elif switch_condition == aw.layout.PageLayoutEvent.CONVERSION_FINISHED:
            self._notify_conversion_finished(a)

    def _notify_part_finished(self, a):
        print(f'Part at page {a.page_index + 1} reflow.')
        self._render_page(a, a.page_index)

    def _notify_conversion_finished(self, a):
        print(f'Document "{a.document.built_in_document_properties.title}" converted to page format.')

    def _render_page(self, a, page_index):
        from pathlib import Path
        import aspose.words as aw
        from api_example_base import ApiExampleBase, ARTIFACTS_DIR
        save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)
        save_options.page_set = aw.saving.PageSet(page=page_index)
        mNum += 1
        file_path = Path(ARTIFACTS_DIR) / f'PageLayoutCallback.page-{pageIndex + 1} {mNum}.png'
        with open(file_path, 'wb') as stream:
            a.document.save(stream, save_options)
```

### See Also

* module [aspose.words.layout](../)
* property [LayoutOptions.callback](../layoutoptions/callback/)

