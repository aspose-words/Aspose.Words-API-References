---
title: TxtLoadOptions.trailing_spaces_options property
linktitle: trailing_spaces_options property
articleTitle: trailing_spaces_options property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.trailing_spaces_options property. Gets or sets preferred option of a trailing space handling"
type: docs
weight: 70
url: /es/python-net/aspose.words.loading/txtloadoptions/trailing_spaces_options/
---

## TxtLoadOptions.trailing_spaces_options property

Gets or sets preferred option of a trailing space handling.
Default value is [TxtTrailingSpacesOptions.TRIM](../../txttrailingspacesoptions/#TRIM).



```python
@property
def trailing_spaces_options(self) -> aspose.words.loading.TxtTrailingSpacesOptions:
    ...

@trailing_spaces_options.setter
def trailing_spaces_options(self, value: aspose.words.loading.TxtTrailingSpacesOptions):
    ...

```

### Examples

Shows how to trim whitespace when loading plaintext documents.

```python
text_doc = '      Line 1 \n' + '    Line 2   \n' + ' Line 3       '
# Cree un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
# para modificar cómo cargamos un documento de texto sin formato.
load_options = aw.loading.TxtLoadOptions()
# Establezca la propiedad "LeadingSpacesOptions" a "TxtLeadingSpacesOptions.Preserve"
# para preservar todos los caracteres de espacio en blanco al inicio de cada línea.
# Establezca la propiedad "LeadingSpacesOptions" a "TxtLeadingSpacesOptions.ConvertToIndent"
# para eliminar todos los caracteres de espacio en blanco al inicio de cada línea,
# y luego aplique una sangría izquierda en la primera línea al párrafo para simular el efecto de los espacios en blanco.
# Establezca la propiedad "LeadingSpacesOptions" a "TxtLeadingSpacesOptions.Trim"
# para eliminar todos los caracteres de espacio en blanco del inicio de cada línea.
load_options.leading_spaces_options = txt_leading_spaces_options
# Establezca la propiedad "TrailingSpacesOptions" a "TxtTrailingSpacesOptions.Preserve"
# para conservar todos los caracteres de espacio en blanco al final de cada línea.
# Establezca la propiedad "TrailingSpacesOptions" a "TxtTrailingSpacesOptions.Trim" para
# eliminar todos los caracteres de espacio en blanco del final de cada línea.
load_options.trailing_spaces_options = txt_trailing_spaces_options
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(text_doc, system_helper.text.Encoding.utf_8())), load_options=load_options)
paragraphs = doc.first_section.body.paragraphs
switch_condition = txt_leading_spaces_options
if switch_condition == aw.loading.TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
    self.assertEqual(37.8, paragraphs[0].paragraph_format.first_line_indent)
    self.assertEqual(25.2, paragraphs[1].paragraph_format.first_line_indent)
    self.assertEqual(6.3, paragraphs[2].paragraph_format.first_line_indent)
    self.assertTrue(paragraphs[0].get_text().startswith('Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith('Line 3'))
elif switch_condition == aw.loading.TxtLeadingSpacesOptions.PRESERVE:
    self.assertTrue(all([p.as_paragraph().paragraph_format.first_line_indent == 0 for p in paragraphs]))
    self.assertTrue(paragraphs[0].get_text().startswith('      Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('    Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith(' Line 3'))
elif switch_condition == aw.loading.TxtLeadingSpacesOptions.TRIM:
    self.assertTrue(all([p.as_paragraph().paragraph_format.first_line_indent == 0 for p in paragraphs]))
    self.assertTrue(paragraphs[0].get_text().startswith('Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith('Line 3'))
switch_condition = txt_trailing_spaces_options
if switch_condition == aw.loading.TxtTrailingSpacesOptions.PRESERVE:
    self.assertTrue(paragraphs[0].get_text().endswith('Line 1 \r'))
    self.assertTrue(paragraphs[1].get_text().endswith('Line 2   \r'))
    self.assertTrue(paragraphs[2].get_text().endswith('Line 3       \x0c'))
elif switch_condition == aw.loading.TxtTrailingSpacesOptions.TRIM:
    self.assertTrue(paragraphs[0].get_text().endswith('Line 1\r'))
    self.assertTrue(paragraphs[1].get_text().endswith('Line 2\r'))
    self.assertTrue(paragraphs[2].get_text().endswith('Line 3\x0c'))
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

