---
title: PsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "PsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /de/python-net/aspose.words.saving/pssaveoptions/save_format/
---

## PsSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.PS](../../../aspose.words/saveformat/#PS).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

### Examples

Shows how to save a document to the Postscript format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Erstellen Sie ein "PsSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in PostScript konvertiert.
# Setzen Sie die Eigenschaft "UseBookFoldPrintingSettings" auf "true", um den Inhalt
# im ausgegebenen Postscript-Dokument so anzuordnen, dass wir daraus ein Heft erstellen können.
# Setzen Sie die Eigenschaft "UseBookFoldPrintingSettings" auf "false", um das Dokument normal zu speichern.
save_options = aw.saving.PsSaveOptions()
save_options.save_format = aw.SaveFormat.PS
save_options.use_book_fold_printing_settings = render_text_as_book_fold
# Wenn wir das Dokument als Heft rendern, müssen wir die "MultiplePages" setzen
# Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte auf "MultiplePagesType.BookFoldPrinting" setzen.
for s in doc.sections:
    s = s.as_section()
    s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Sobald wir dieses Dokument beidseitig drucken, können wir alle Seiten gleichzeitig in der Mitte falten,
# und der Inhalt wird sich so ausrichten, dass ein Heft entsteht.
doc.save(file_name=ARTIFACTS_DIR + 'PsSaveOptions.UseBookFoldPrintingSettings.ps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PsSaveOptions](../)

