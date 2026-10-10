---
title: XpsSaveOptions constructor
linktitle: XpsSaveOptions constructor
articleTitle: XpsSaveOptions constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.XpsSaveOptions constructor"
type: docs
weight: 10
url: /de/python-net/aspose.words.saving/xpssaveoptions/__init__/
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

## See Also

* module [aspose.words.saving](../../)
* class [XpsSaveOptions](../)

