---
title: SvgSaveOptions.id_prefix property
linktitle: id_prefix property
articleTitle: id_prefix property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.id_prefix property. Specifies a prefix that is prepended to all generated element IDs in the output document"
type: docs
weight: 40
url: /python-net/aspose.words.saving/svgsaveoptions/id_prefix/
---

## SvgSaveOptions.id_prefix property

Specifies a prefix that is prepended to all generated element IDs in the output document.
Default value is null and no prefix is prepended.


```python
@property
def id_prefix(self) -> str:
    ...

@id_prefix.setter
def id_prefix(self, value: str):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | The value does not meet the requirements specified above. |

### Remarks

If the prefix is specified, it can contain only letters, digits, underscores, and hyphens,
and must start with a letter.


### Examples

Shows how to add a prefix that is prepended to all generated element IDs (svg).

```python
doc = aw.Document(file_name=MY_DIR + 'Id prefix.docx')
save_options = aw.saving.SvgSaveOptions()
save_options.id_prefix = 'pfx1_'
doc.save(file_name=ARTIFACTS_DIR + 'SvgSaveOptions.IdPrefixSvg.html', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SvgSaveOptions](../)

