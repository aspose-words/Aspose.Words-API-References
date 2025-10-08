---
title: PdfSaveOptions.render_choice_form_field_border property
linktitle: render_choice_form_field_border property
articleTitle: render_choice_form_field_border property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.render_choice_form_field_border property. Specifies whether to render PDF choice form field border."
type: docs
weight: 300
url: /python-net/aspose.words.saving/pdfsaveoptions/render_choice_form_field_border/
---

## PdfSaveOptions.render_choice_form_field_border property

Specifies whether to render PDF choice form field border.


```python
@property
def render_choice_form_field_border(self) -> bool:
    ...

@render_choice_form_field_border.setter
def render_choice_form_field_border(self, value: bool):
    ...

```

### Remarks

PDF choice form fields are used for export of SDT Combo Box Content Control, SDT Drop-Down List Content
Control and legacy Drop-Down Form Field when [PdfSaveOptions.preserve_form_fields](../preserve_form_fields/) option is enabled.

The default value is ``True``.




### Examples

Shows how to render PDF choice form field border.

```python
doc = aw.Document(file_name=MY_DIR + 'Legacy drop-down.docx')
save_options = aw.saving.PdfSaveOptions()
save_options.preserve_form_fields = True
save_options.render_choice_form_field_border = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.RenderChoiceFormFieldBorder.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

