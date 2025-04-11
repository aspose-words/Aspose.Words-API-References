---
title: HtmlSaveOptions.remove_java_script_from_links property
linktitle: remove_java_script_from_links property
articleTitle: remove_java_script_from_links property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.remove_java_script_from_links property. Specifies whether JavaScript will be removed from links"
type: docs
weight: 410
url: /python-net/aspose.words.saving/htmlsaveoptions/remove_java_script_from_links/
---

## HtmlSaveOptions.remove_java_script_from_links property

Specifies whether JavaScript will be removed from links.
Default is ``False``.



```python
@property
def remove_java_script_from_links(self) -> bool:
    ...

@remove_java_script_from_links.setter
def remove_java_script_from_links(self, value: bool):
    ...

```

### Remarks

If this option is enabled, all links containing JavaScript (e.g., links with "javascript:" in the href attribute)
will be replaced with "javascript:void(0)". This can help prevent potential security risks, such as XSS attacks.


### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

