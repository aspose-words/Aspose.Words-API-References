---
title: HtmlSaveOptions.replace_backslash_with_yen_sign property
linktitle: replace_backslash_with_yen_sign property
articleTitle: replace_backslash_with_yen_sign property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.replace_backslash_with_yen_sign property. Specifies whether backslash characters should be replaced with yen signs"
type: docs
weight: 410
url: /python-net/aspose.words.saving/htmlsaveoptions/replace_backslash_with_yen_sign/
---

## HtmlSaveOptions.replace_backslash_with_yen_sign property

Specifies whether backslash characters should be replaced with yen signs.
Default value is ``False``.



```python
@property
def replace_backslash_with_yen_sign(self) -> bool:
    ...

@replace_backslash_with_yen_sign.setter
def replace_backslash_with_yen_sign(self, value: bool):
    ...

```

### Remarks

By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.


### Examples

Shows how to replace backslash characters with yen signs (Html).

```python
doc = aw.Document(file_name=MY_DIR + 'Korean backslash symbol.docx')
# By default, Aspose.Words mimics MS Word's behavior and doesn't replace backslash characters with yen signs in
# generated HTML documents. However, previous versions of Aspose.Words performed such replacements in certain
# scenarios. This flag enables backward compatibility with previous versions of Aspose.Words.
save_options = aw.saving.HtmlSaveOptions()
save_options.replace_backslash_with_yen_sign = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.ReplaceBackslashWithYenSign.html', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

