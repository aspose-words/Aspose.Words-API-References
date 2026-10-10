---
title: TxtSaveOptions.simplify_list_labels property
linktitle: simplify_list_labels property
articleTitle: simplify_list_labels property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.simplify_list_labels property. Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text."
type: docs
weight: 80
url: /fr/python-net/aspose.words.saving/txtsaveoptions/simplify_list_labels/
---

## TxtSaveOptions.simplify_list_labels property

Specifies whether the program should simplify list labels in case of
complex label formatting not being adequately represented by plain text.

If set to ``True``, numbered list labels are written in simple numeric format
and itemized list labels as simple ASCII characters. The default value is ``False``.




```python
@property
def simplify_list_labels(self) -> bool:
    ...

@simplify_list_labels.setter
def simplify_list_labels(self, value: bool):
    ...

```

### Examples

Shows how to change the appearance of lists when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Créez une liste à puces avec cinq niveaux d'indentation.
builder.list_format.apply_bullet_default()
builder.writeln('Item 1')
builder.list_format.list_indent()
builder.writeln('Item 2')
builder.list_format.list_indent()
builder.writeln('Item 3')
builder.list_format.list_indent()
builder.writeln('Item 4')
builder.list_format.list_indent()
builder.write('Item 5')
# Créez un objet "TxtSaveOptions", que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont nous enregistrons le document en texte brut.
txt_save_options = aw.saving.TxtSaveOptions()
# Définissez la propriété "SimplifyListLabels" sur "true" pour convertir certains éléments de liste
# en caractères ASCII plus simples, tels que '*', 'o', '+', '>', etc.
# Définissez la propriété "SimplifyListLabels" sur "false" pour préserver autant que possible les symboles de liste d'origine.
txt_save_options.simplify_list_labels = simplify_list_labels
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.SimplifyListLabels.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.SimplifyListLabels.txt')
new_line = system_helper.environment.Environment.new_line()
if simplify_list_labels:
    self.assertEqual(f'* Item 1{new_line}' + f'  > Item 2{new_line}' + f'    + Item 3{new_line}' + f'      - Item 4{new_line}' + f'        o Item 5{new_line}', doc_text)
else:
    self.assertEqual(f'· Item 1{new_line}' + f'o Item 2{new_line}' + f'§ Item 3{new_line}' + f'· Item 4{new_line}' + f'o Item 5{new_line}', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

