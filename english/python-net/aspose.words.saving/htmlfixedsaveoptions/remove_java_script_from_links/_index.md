---
title: HtmlFixedSaveOptions.remove_java_script_from_links property
linktitle: remove_java_script_from_links property
articleTitle: remove_java_script_from_links property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.remove_java_script_from_links property. Specifies whether JavaScript will be removed from links"
type: docs
weight: 140
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/remove_java_script_from_links/
---

## HtmlFixedSaveOptions.remove_java_script_from_links property

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


### Examples

Shows how to remove JavaScript from the links for html fixed documents.

```python
doc = aw.Document(file_name=MY_DIR + 'JavaScript in HREF.docx')
save_options = aw.saving.HtmlFixedSaveOptions()
save_options.remove_java_script_from_links = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html', save_options=save_options)
```

Shows how to remove JavaScript from the links.

```python
doc = aw.Document(file_name=MY_DIR + 'JavaScript in HREF.docx')
save_options = aw.saving.HtmlSaveOptions()
save_options.remove_java_script_from_links = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.RemoveJavaScriptFromLinks.html', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

