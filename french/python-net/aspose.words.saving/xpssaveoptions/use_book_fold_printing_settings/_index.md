---
title: XpsSaveOptions.use_book_fold_printing_settings property
linktitle: use_book_fold_printing_settings property
articleTitle: use_book_fold_printing_settings property
second_title: Aspose.Words for Python
description: "XpsSaveOptions.use_book_fold_printing_settings property. Gets or sets a boolean value indicating whether the document should be saved using a booklet printing layout, if it is specified via [PageSetup.multiple_pages](../../../aspose.words/pagesetup/multiple_pages/)."
type: docs
weight: 60
url: /fr/python-net/aspose.words.saving/xpssaveoptions/use_book_fold_printing_settings/
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
# Créez un objet "XpsSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .XPS.
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# Définissez la propriété "UseBookFoldPrintingSettings" sur "true" pour organiser le contenu
# dans le XPS de sortie d'une manière qui nous aide à l'utiliser pour créer un livret.
# Définissez la propriété "UseBookFoldPrintingSettings" sur "false" pour rendre le XPS normalement.
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# Si nous rendons le document sous forme de livret, nous devons définir le "MultiplePages"
# les propriétés des objets de configuration de page de toutes les sections à "MultiplePagesType.BookFoldPrinting".
if render_text_as_book_fold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# Une fois que nous imprimons ce document, nous pouvons le transformer en livret en empilant les pages
# qui sortent de l'imprimante et en les pliant au milieu.
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.BookFold.xps', save_options=xps_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

