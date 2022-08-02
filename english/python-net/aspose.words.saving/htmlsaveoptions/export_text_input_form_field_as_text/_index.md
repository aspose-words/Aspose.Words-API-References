---
title: export_text_input_form_field_as_text property
second_title: Aspose.Words for Python via .NET API Reference
description: "Controls how text input form fields are saved to HTML or MHTML"
type: docs
weight: 280
url: /python-net/aspose.words.saving/htmlsaveoptions/export_text_input_form_field_as_text/
---

## HtmlSaveOptions.export_text_input_form_field_as_text property

Controls how text input form fields are saved to HTML or MHTML.
Default value is ``false``.


When set to ``true``, exports text input form fields as normal text. 
When ``false``, exports Word text input form fields as INPUT elements in HTML.

When exporting to EPUB, text input form fields are always saved as text due 
to requirements of this format.




### Examples

Shows how to specify the folder for storing linked images after saving to .html.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

images_dir = os.path.join(ARTIFACTS_DIR, "SaveHtmlWithOptions")

if os.path.exists(images_dir):
    shutil.rmtree(images_dir)

os.makedirs(images_dir)

# Set an option to export form fields as plain text instead of HTML input elements.
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.export_text_input_form_field_as_text = True
options.images_folder = images_dir

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.image_folder.html", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

