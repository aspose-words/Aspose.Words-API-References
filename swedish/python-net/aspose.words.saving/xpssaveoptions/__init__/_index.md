---
title: XpsSaveOptions constructor
linktitle: XpsSaveOptions constructor
articleTitle: XpsSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.XpsSaveOptions constructor"
type: docs
weight: 10
url: /sv/python-net/aspose.words.saving/xpssaveoptions/__init__/
---

## XpsSaveOptions() {#default}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS) format.



```python
def __init__(self):
    ...
```

## XpsSaveOptions(save_format) {#saveformat}

Initializes a new instance of this class that can be used to save a document
in the [SaveFormat.XPS](../../../aspose.words/saveformat/#XPS) or [SaveFormat.OPEN_XPS](../../../aspose.words/saveformat/#OPEN_XPS) format.



```python
def __init__(self, save_format: aspose.words.SaveFormat):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| save_format | [SaveFormat](../../../aspose.words/saveformat/) |  |

## Examples

Shows how to save a document to the XPS format in the form of a book fold.

```python
doc = aw.Document(file_name=MY_DIR + 'Paragraphs.docx')
# Skapa ett "XpsSaveOptions"‑objekt som vi kan skicka till dokumentets "Save"‑metod
# för att ändra hur den metoden konverterar dokumentet till .XPS.
xps_options = aw.saving.XpsSaveOptions(aw.SaveFormat.XPS)
# Ställ in egenskapen "UseBookFoldPrintingSettings" till "true" för att ordna innehållet
# i den exporterade XPS‑filen på ett sätt som hjälper oss att använda den för att skapa en häfte.
# Ställ in egenskapen "UseBookFoldPrintingSettings" till "false" för att rendera XPS‑filen normalt.
xps_options.use_book_fold_printing_settings = render_text_as_book_fold
# Om vi renderar dokumentet som en häfte, måste vi sätta "MultiplePages"
# egenskaperna för sidinställningsobjekten i alla sektioner till "MultiplePagesType.BookFoldPrinting".
if render_text_as_book_fold:
    for s in doc.sections:
        s = s.as_section()
        s.page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# När vi skriver ut detta dokument kan vi göra det till ett häfte genom att stapla sidorna
# så att de kommer ur skrivaren och viks på mitten.
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.BookFold.xps', save_options=xps_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

