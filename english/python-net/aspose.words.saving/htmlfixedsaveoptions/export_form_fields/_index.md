---
title: export_form_fields property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics."
type: docs
weight: 80
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/export_form_fields/
---

## HtmlFixedSaveOptions.export_form_fields property

Gets or sets indication of whether form fields are exported as interactive
items (as 'input' tag) rather than converted to text or graphics.


### Examples

Shows how to export form fields to Html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_check_box("CheckBox", False, 15)

# When we export a document with form fields to .html,
# there are two ways in which Aspose.Words can export form fields.
# Setting the "export_form_fields" flag to "True" will export them as interactive objects.
# Setting this flag to "False" will display form fields as plain text.
# This will freeze them at their current value, and prevent the reader of our HTML document
# from being able to interact with them.
html_fixed_save_options = aw.saving.HtmlFixedSaveOptions()
html_fixed_save_options.export_form_fields = export_form_fields

doc.save(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_form_fields.html", html_fixed_save_options)

with open(ARTIFACTS_DIR + "HtmlFixedSaveOptions.export_form_fields.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if export_form_fields:
    self.assertRegex(out_doc_contents,
        '<a name="CheckBox" style="left:0pt; top:0pt;"></a>' +
        '<input style="position:absolute; left:0pt; top:0pt;" type="checkbox" name="CheckBox" />')
else:
    self.assertRegex(out_doc_contents,
        '<a name="CheckBox" style="left:0pt; top:0pt;"></a>' +
        '<div class="awdiv" style="left:0.8pt; top:0.8pt; width:14.25pt; height:14.25pt; border:solid 0.75pt #000000;"')
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

