---
title: HtmlSaveOptions.export_drop_down_form_field_as_text property
linktitle: export_drop_down_form_field_as_text property
articleTitle: export_drop_down_form_field_as_text property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_drop_down_form_field_as_text property. Controls how drop-down form fields are saved to HTML or MHTML"
type: docs
weight: 130
url: /python-net/aspose.words.saving/htmlsaveoptions/export_drop_down_form_field_as_text/
---

## HtmlSaveOptions.export_drop_down_form_field_as_text property

Controls how drop-down form fields are saved to HTML or MHTML.
Default value is ``False``.



```python
@property
def export_drop_down_form_field_as_text(self) -> bool:
    ...

@export_drop_down_form_field_as_text.setter
def export_drop_down_form_field_as_text(self, value: bool):
    ...

```

### Remarks

When set to ``True``, exports drop-down form fields as normal text.
When ``False``, exports drop-down form fields as SELECT element in HTML.

When exporting to EPUB, text drop-down form fields are always saved as text due 
to requirements of this format.




### Examples

Shows how to get drop-down combo box form fields to blend in with paragraph text when saving to html.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Use a document builder to insert a combo box with the value "Two" selected.
builder.insert_combo_box("MyComboBox", ["One", "Two", "Three"], 1)

# The "export_drop_down_form_field_as_text" flag of this SaveOptions object allows us to
# control how saving the document to HTML treats drop-down combo boxes.
# Setting it to "True" will convert each combo box into simple text
# that displays the combo box's currently selected value, effectively freezing it.
# Setting it to "False" will preserve the functionality of the combo box using <select> and <option> tags.
options = aw.saving.HtmlSaveOptions()
options.export_drop_down_form_field_as_text = export_drop_down_form_field_as_text

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.drop_down_form_field.html", options)

with open(ARTIFACTS_DIR + "HtmlSaveOptions.drop_down_form_field.html", "rt", encoding="utf-8") as file:
    out_doc_contents = file.read()

if export_drop_down_form_field_as_text:
    self.assertIn("<span>Two</span>", out_doc_contents)
else:
    self.assertIn(
        "<select name=\"MyComboBox\">" +
            "<option>One</option>" +
            "<option selected=\"selected\">Two</option>" +
            "<option>Three</option>" +
        "</select>",
        out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

