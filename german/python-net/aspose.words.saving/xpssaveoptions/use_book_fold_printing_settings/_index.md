---
title: XpsSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 60
url: /de/python-net/aspose.words.saving/xpssaveoptions/use_book_fold_printing_settings/
---

## XpsSaveOptions.use_book_fold_printing_settings property

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

Shows how to save a document to the XPS format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Erstellen Sie ein "XpsSaveOptions"‑Objekt, das wir an die "Save"‑Methode des Dokuments übergeben können
# um zu ändern, wie diese Methode das Dokument in .XPS konvertiert.
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# Setzen Sie die Eigenschaft "UseBookFoldPrintingSettings" auf "true", um den Inhalt
# im ausgegebenen XPS auf eine Weise, die uns hilft, es zu einem Heft zu machen.
# Setzen Sie die Eigenschaft \"UseBookFoldPrintingSettings\" auf \"false\", um das XPS normal zu rendern.
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# Wenn wir das Dokument als Heft rendern, müssen wir die "MultiplePages" setzen
# Eigenschaften der Seiteneinrichtungsobjekte aller Abschnitte auf "MultiplePagesType.BookFoldPrinting" setzen.
if render_text_as_book_fold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Sobald wir dieses Dokument drucken, können wir es zu einem Heft machen, indem wir die Seiten stapeln
# die aus dem Drucker kommen und in der Mitte falten.
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.BookFold.xps', save_options=xps_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

