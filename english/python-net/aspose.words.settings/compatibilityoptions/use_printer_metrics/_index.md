---
title: CompatibilityOptions.use_printer_metrics property
linktitle: use_printer_metrics property
articleTitle: use_printer_metrics property
second_title: Aspose.Words for Python
description: "CompatibilityOptions.use_printer_metrics property. Use Printer Metrics To Display Documents."
type: docs
weight: 640
url: /python-net/aspose.words.settings/compatibilityoptions/use_printer_metrics/
---

## CompatibilityOptions.use_printer_metrics property

Use Printer Metrics To Display Documents.


```python
@property
def use_printer_metrics(self) -> bool:
    ...

@use_printer_metrics.setter
def use_printer_metrics(self, value: bool):
    ...

```

### Remarks

Printer Metrics may differ depending on drivers used.
For instance, Windows "Microsoft OpenXPS Class Driver 2" and "Microsoft Print to PDF" provide slightly different metrics.
Therefore, the final document's layout may change if this option is enabled.


### See Also

* module [aspose.words.settings](../../)
* class [CompatibilityOptions](../)

