---
title: PageLayoutCallbackArgs.page_index property
linktitle: page_index property
articleTitle: page_index property
second_title: Aspose.Words for Python
description: "PageLayoutCallbackArgs.page_index property. Gets 0-based index of the page in the document this event relates to"
type: docs
weight: 30
url: /python-net/aspose.words.layout/pagelayoutcallbackargs/page_index/
---

## PageLayoutCallbackArgs.page_index property

Gets 0-based index of the page in the document this event relates to.
Returns negative value if there is no associated page, or if page was removed during reflow.


```python
@property
def page_index(self) -> int:
    ...

```

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

* module [aspose.words.layout](../../)
* class [PageLayoutCallbackArgs](../)

