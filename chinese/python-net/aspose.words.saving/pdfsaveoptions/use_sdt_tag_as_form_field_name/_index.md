---
title: PdfSaveOptions.use_sdt_tag_as_form_field_name property
linktitle: use_sdt_tag_as_form_field_name property
articleTitle: use_sdt_tag_as_form_field_name property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.use_sdt_tag_as_form_field_name property. Specifies whether to use SDT control Tag or Id property as a name of form field in PDF."
type: docs
weight: 360
url: /zh/python-net/aspose.words.saving/pdfsaveoptions/use_sdt_tag_as_form_field_name/
---

## PdfSaveOptions.use_sdt_tag_as_form_field_name property

Specifies whether to use SDT control Tag or Id property as a name of form field in PDF.


```python
@property
def use_sdt_tag_as_form_field_name(self) -> bool:
    ...

@use_sdt_tag_as_form_field_name.setter
def use_sdt_tag_as_form_field_name(self, value: bool):
    ...

```

### Remarks

The default value is ``False``.

When set to ``False``, SDT control Id property is used as a name of form field in PDF.

When set to ``True``, SDT control Tag property is used as a name of form field in PDF.

If set to ``True`` and Tag is empty, Id property will be used as a form field name.

If set to ``True`` and Tag values are not unique, duplicate Tag values will be altered to build
unique PDF form field names.




### Examples

Shows how to use SDT control Tag or Id property as a name of form field in PDF.

```python
doc = aw.Document(file_name=MY_DIR + 'Form fields.docx')
save_options = aw.saving.PdfSaveOptions()
save_options.preserve_form_fields = True
# 当设置为 'false' 时，SDT 控件 Id 属性用作 PDF 中表单字段的名称。
# 当设置为 'true' 时，SDT 控件 Tag 属性用作 PDF 中表单字段的名称。
save_options.use_sdt_tag_as_form_field_name = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.SdtTagAsFormFieldName.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

