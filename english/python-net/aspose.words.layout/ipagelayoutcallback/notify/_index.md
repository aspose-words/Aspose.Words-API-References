---
title: IPageLayoutCallback.notify method
linktitle: notify method
articleTitle: notify method
second_title: Aspose.Words for Python
description: "IPageLayoutCallback.notify method. This is called to notify of layout build and rendering progress."
type: docs
weight: 10
url: /python-net/aspose.words.layout/ipagelayoutcallback/notify/
---

## notify(args) {#pagelayoutcallbackargs}

This is called to notify of layout build and rendering progress.


```python
def notify(self, args: aspose.words.layout.PageLayoutCallbackArgs):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| args | [PageLayoutCallbackArgs](../../pagelayoutcallbackargs/) | An argument of the event. |

### Remarks

Exception when thrown by implementation aborts layout build process.




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
* class [IPageLayoutCallback](../)

