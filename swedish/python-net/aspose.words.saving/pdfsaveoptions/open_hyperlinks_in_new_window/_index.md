---
title: PdfSaveOptions.open_hyperlinks_in_new_window property
linktitle: open_hyperlinks_in_new_window property
articleTitle: open_hyperlinks_in_new_window property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.open_hyperlinks_in_new_window property. Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser."
type: docs
weight: 250
url: /sv/python-net/aspose.words.saving/pdfsaveoptions/open_hyperlinks_in_new_window/
---

## PdfSaveOptions.open_hyperlinks_in_new_window property

Gets or sets a value determining whether hyperlinks in the output Pdf document
are forced to be opened in a new window (or tab) of a browser.


```python
@property
def open_hyperlinks_in_new_window(self) -> bool:
    ...

@open_hyperlinks_in_new_window.setter
def open_hyperlinks_in_new_window(self, value: bool):
    ...

```

### Remarks

The default value is ``False``. When this value is set to ``True``
hyperlinks are saved using JavaScript code.
JavaScript code is ``app.launchURL("URL", true);``,
where ``URL`` is a hyperlink.


Note that if this option is set to ``True`` hyperlinks can't work
in some PDF readers e.g. Chrome, Firefox.


JavaScript actions are prohibited by PDF/A-1, PDF/A-2 and PDF/A-3 compliance.
The ``False`` value will be used automatically in this case.




### Examples

Shows how to save hyperlinks in a document we convert to PDF so that they open new pages when we click on them.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_hyperlink('Testlink', 'https://www.google.com/search?q=%20aspose', False)
# Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .PDF.
options = aw.saving.PdfSaveOptions()
# Ställ in egenskapen "OpenHyperlinksInNewWindow" till "true" för att spara alla hyperlänkar med Javascript‑kod
# som tvingar läsare att öppna dessa länkar i nya fönster/webbläsarflikar.
# Ställ in egenskapen "OpenHyperlinksInNewWindow" till "false" för att spara alla hyperlänkar normalt.
options.open_hyperlinks_in_new_window = open_hyperlinks_in_new_window
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.OpenHyperlinksInNewWindow.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

