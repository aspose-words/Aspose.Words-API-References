---
title: PsSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "PsSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 20
url: /sv/python-net/aspose.words.saving/pssaveoptions/save_format/
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
# Skapa ett "PsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till PostScript.
# Ställ in egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
# i den resulterande Postscript-dokumentet på ett sätt som hjälper oss att göra en häfte av det.
# Ställ in egenskapen "UseBookFoldPrintingSettings" till "false" för att spara dokumentet normalt.
save_options = aw.saving.PsSaveOptions()
save_options.save_format = aw.SaveFormat.PS
save_options.use_book_fold_printing_settings = render_text_as_book_fold
# Om vi renderar dokumentet som en häfte, måste vi sätta "MultiplePages"
# egenskaperna för sidinställningsobjekten i alla sektioner till "MultiplePagesType.BookFoldPrinting".
for s in doc.sections:
    s = s.as_section()
    s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# När vi skriver ut detta dokument på båda sidor av sidorna, kan vi vika alla sidor på mitten på en gång,
# och innehållet kommer att stämma överens på ett sätt som skapar ett häfte.
doc.save(file_name=ARTIFACTS_DIR + 'PsSaveOptions.UseBookFoldPrintingSettings.ps', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PsSaveOptions](../)

