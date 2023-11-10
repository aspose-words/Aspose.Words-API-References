---
title: CompatibilityOptions.ui_compat_97_to_2003 property
linktitle: ui_compat_97_to_2003 property
articleTitle: ui_compat_97_to_2003 property
second_title: Aspose.Words for Python
description: "CompatibilityOptions.ui_compat_97_to_2003 property. True to disable UI functionality which is not compatible with Word97-2003"
type: docs
weight: 570
url: /python-net/aspose.words.settings/compatibilityoptions/ui_compat_97_to_2003/
---

## CompatibilityOptions.ui_compat_97_to_2003 property

True to disable UI functionality which is not compatible with Word97-2003.
Default value is ``False``.



```python
@property
def ui_compat_97_to_2003(self) -> bool:
    ...

@ui_compat_97_to_2003.setter
def ui_compat_97_to_2003(self, value: bool):
    ...

```

### Remarks

Controls the Word97-2003 compatibility setting that disables UI functionality which
is not compatible with Word97-2003.
When ``True``, 'w:uiCompat97To2003' XML element is written to '\\word\\settings.xml'
document package part.
Default value is ``False``. When set to ``False``, this element is not written.

Technically this property is not part of compatibility options, but we have put it here for API convenience.



### See Also

* module [aspose.words.settings](../../)
* class [CompatibilityOptions](../)

