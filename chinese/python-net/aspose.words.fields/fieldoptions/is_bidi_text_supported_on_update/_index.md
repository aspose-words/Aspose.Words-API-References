---
title: FieldOptions.is_bidi_text_supported_on_update property
linktitle: is_bidi_text_supported_on_update property
articleTitle: is_bidi_text_supported_on_update property
second_title: Aspose.Words for Python
description: "FieldOptions.is_bidi_text_supported_on_update property. Gets or sets the value indicating whether bidirectional text is fully supported during field update or not."
type: docs
weight: 150
url: /zh/python-net/aspose.words.fields/fieldoptions/is_bidi_text_supported_on_update/
---

## FieldOptions.is_bidi_text_supported_on_update property

Gets or sets the value indicating whether bidirectional text is fully supported during field update or not.


```python
@property
def is_bidi_text_supported_on_update(self) -> bool:
    ...

@is_bidi_text_supported_on_update.setter
def is_bidi_text_supported_on_update(self, value: bool):
    ...

```

### Remarks

When this property is set to ``True``, additional steps are performed to produce Right-To-Left language
(i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to ``False`` and Right-To-Left language is used, correctness of field result
after its update is not guaranteed.

The default value is ``False``.




### Examples

Shows how to use FieldOptions to ensure that field updating fully supports bi-directional text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 确保任何涉及从右到左文本的字段操作都按预期执行。
doc.field_options.is_bidi_text_supported_on_update = True
# 使用文档生成器插入包含从右到左文本的字段。
combo_box = builder.insert_combo_box('MyComboBox', ['עֶשְׂרִים', 'שְׁלוֹשִׁים', 'אַרְבָּעִים', 'חֲמִשִּׁים', 'שִׁשִּׁים'], 0)
combo_box.calculate_on_exit = True
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'FieldOptions.Bidi.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

