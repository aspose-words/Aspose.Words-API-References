---
title: PsSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "PsSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 30
url: /de/python-net/aspose.words.saving/pssaveoptions/use_book_fold_printing_settings/
---

## PsSaveOptions.use_book_fold_printing_settings property

Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout,
if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/).



```python
@property
def use_book_fold_printing_settings(self) -> bool:
    ...

@use_book_fold_printing_settings.setter
def use_book_fold_printing_settings(self, value: bool):
    ...

```

### Remarks

If this option is specified, [FixedPageSaveOptions.page_set](../../fixedpagesaveoptions/page_set/) is ignored when saving.
This behavior matches MS Word.
If book fold printing settings are not specified in page setup, this option will have no effect.





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

