---
title: LayoutOptions.ignore_printer_metrics property
linktitle: ignore_printer_metrics property
articleTitle: ignore_printer_metrics property
second_title: Aspose.Words for Python
description: "LayoutOptions.ignore_printer_metrics property. Gets or sets indication of whether the Use printer metrics to lay out document compatibility option is ignored"
type: docs
weight: 50
url: /python-net/aspose.words.layout/layoutoptions/ignore_printer_metrics/
---

## LayoutOptions.ignore_printer_metrics property

Gets or sets indication of whether the "Use printer metrics to lay out document" compatibility option is ignored.
Default is ``True``.



```python
@property
def ignore_printer_metrics(self) -> bool:
    ...

@ignore_printer_metrics.setter
def ignore_printer_metrics(self, value: bool):
    ...

```

### Examples

Shows how to ignore 'Use printer metrics to lay out document' option.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.layout_options.ignore_printer_metrics = False
doc.save(file_name=ARTIFACTS_DIR + 'Document.IgnorePrinterMetrics.docx')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

