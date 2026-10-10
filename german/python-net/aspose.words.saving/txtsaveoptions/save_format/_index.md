---
title: TxtSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 70
url: /de/python-net/aspose.words.saving/txtsaveoptions/save_format/
---

## TxtSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.TEXT](../../../aspose.words/saveformat/#TEXT).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a .txt document with a custom paragraph break.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
builder.write('Paragraph 3.')
# Erstellen Sie ein "TxtSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
# um zu ändern, wie wir das Dokument als Klartext speichern.
txt_save_options = aw.saving.TxtSaveOptions()
self.assertEqual(aw.SaveFormat.TEXT, txt_save_options.save_format)
# Setzen Sie den "ParagraphBreak" auf einen benutzerdefinierten Wert, den wir am Ende jedes Absatzes einfügen möchten.
txt_save_options.paragraph_break = ' End of paragraph.\n\n\t'
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.ParagraphBreak.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.ParagraphBreak.txt')
self.assertEqual('Paragraph 1. End of paragraph.\n\n\t' + 'Paragraph 2. End of paragraph.\n\n\t' + 'Paragraph 3. End of paragraph.\n\n\t', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

