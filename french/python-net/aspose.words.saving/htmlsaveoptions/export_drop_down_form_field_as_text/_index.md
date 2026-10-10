---
title: HtmlSaveOptions.export_drop_down_form_field_as_text property
linktitle: export_drop_down_form_field_as_text property
articleTitle: export_drop_down_form_field_as_text property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_drop_down_form_field_as_text property. Controls how drop-down form fields are saved to HTML or MHTML"
type: docs
weight: 130
url: /fr/python-net/aspose.words.saving/htmlsaveoptions/export_drop_down_form_field_as_text/
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
builder = aw.DocumentBuilder(doc=doc)
# Utilisez un constructeur de document pour insérer une zone de liste déroulante avec la valeur "Two" sélectionnée.
builder.insert_combo_box('MyComboBox', ['One', 'Two', 'Three'], 1)
# Le drapeau "ExportDropDownFormFieldAsText" de cet objet SaveOptions nous permet de
# contrôler la façon dont l'enregistrement du document en HTML traite les zones de liste déroulante.
# Le définir sur "true" convertira chaque zone de liste déroulante en texte simple
# qui affiche la valeur actuellement sélectionnée de la zone de liste déroulante, la figant effectivement.
# Le définir sur "false" préservera la fonctionnalité de la zone de liste déroulante en utilisant les balises <select> et <option>.
options = aw.saving.HtmlSaveOptions()
options.export_drop_down_form_field_as_text = export_drop_down_form_field_as_text
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.DropDownFormField.html', save_options=options)
out_doc_contents = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'HtmlSaveOptions.DropDownFormField.html')
if export_drop_down_form_field_as_text:
    self.assertTrue('<span>Two</span>' in out_doc_contents)
else:
    self.assertTrue('<select name="MyComboBox">' + '<option>One</option>' + '<option selected="selected">Two</option>' + '<option>Three</option>' + '</select>' in out_doc_contents)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

