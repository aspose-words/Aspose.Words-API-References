---
title: PdfSaveOptions.generate_form_field_scripts property
linktitle: generate_form_field_scripts property
articleTitle: generate_form_field_scripts property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.generate_form_field_scripts property. Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF"
type: docs
weight: 190
url: /python-net/aspose.words.saving/pdfsaveoptions/generate_form_field_scripts/
---

## PdfSaveOptions.generate_form_field_scripts property

Specifies whether to generate scripts that emulate specific Microsoft Word form field behavior in PDF.
Default is ``False``.



```python
@property
def generate_form_field_scripts(self) -> bool:
    ...

@generate_form_field_scripts.setter
def generate_form_field_scripts(self, value: bool):
    ...

```

### Remarks

When this option is enabled, the exporter generates PDF JavaScript actions to emulate Microsoft Word
form field behavior, such as date and time form fields with formatting and validation rules.

When set to ``True``, supported behavior will be exported as PDF JavaScript actions.
When set to ``False``, no form field scripts will be generated.

Script execution depends on the PDF viewer. Some PDF viewers might ignore scripts, restrict script execution,
or require the user to enable JavaScript.

JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance.
The ``False`` value will be used automatically in this case.




### Examples

Shows how to enable generation of JavaScript form field scripts for datetime fields when exporting to PDF.

```python
doc = aw.Document(file_name=MY_DIR + input_file)
# Create save options and enable form field scripts.
# Please note that JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance.
save_options = aw.saving.PdfSaveOptions()
save_options.preserve_form_fields = True
save_options.generate_form_field_scripts = True
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.GenerateFormFieldScriptsDatetime.pdf', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

