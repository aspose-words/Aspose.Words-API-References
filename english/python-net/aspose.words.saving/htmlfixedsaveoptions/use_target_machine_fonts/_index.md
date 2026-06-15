---
title: HtmlFixedSaveOptions.use_target_machine_fonts property
linktitle: use_target_machine_fonts property
articleTitle: use_target_machine_fonts property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.use_target_machine_fonts property. Flag indicates whether fonts from target machine must be used to display the document"
type: docs
weight: 210
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/use_target_machine_fonts/
---

## HtmlFixedSaveOptions.use_target_machine_fonts property

Flag indicates whether fonts from target machine must be used to display the document.
If this flag is set to ``True``, [HtmlFixedSaveOptions.font_format](../font_format/) and [HtmlFixedSaveOptions.export_embedded_fonts](../export_embedded_fonts/) properties do not have effect,
also [HtmlFixedSaveOptions.resource_saving_callback](../resource_saving_callback/) is not fired for fonts.
Default is ``False``.



```python
@property
def use_target_machine_fonts(self) -> bool:
    ...

@use_target_machine_fonts.setter
def use_target_machine_fonts(self, value: bool):
    ...

```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

