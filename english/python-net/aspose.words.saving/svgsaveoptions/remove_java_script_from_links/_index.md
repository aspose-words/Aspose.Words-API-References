---
title: SvgSaveOptions.remove_java_script_from_links property
linktitle: remove_java_script_from_links property
articleTitle: remove_java_script_from_links property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.remove_java_script_from_links property. Specifies whether JavaScript will be removed from links"
type: docs
weight: 60
url: /python-net/aspose.words.saving/svgsaveoptions/remove_java_script_from_links/
---

## SvgSaveOptions.remove_java_script_from_links property

Specifies whether JavaScript will be removed from links.
Default is ``False``.
If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)".



```python
@property
def remove_java_script_from_links(self) -> bool:
    ...

@remove_java_script_from_links.setter
def remove_java_script_from_links(self, value: bool):
    ...

```

### Examples

Shows how to remove JavaScript from the links (svg).

```python
doc = aw.Document(file_name=MY_DIR + 'JavaScript in HREF.docx')
save_options = aw.saving.SvgSaveOptions()
save_options.remove_java_script_from_links = True
doc.save(file_name=ARTIFACTS_DIR + 'SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SvgSaveOptions](../)

