---
title: PdfSaveOptions.open_hyperlinks_in_new_window property
linktitle: open_hyperlinks_in_new_window property
articleTitle: open_hyperlinks_in_new_window property
second_title: Aspose.Words for Python
description: "PdfSaveOptions.open_hyperlinks_in_new_window property. Gets or sets a value determining whether hyperlinks in the output Pdf document are forced to be opened in a new window (or tab) of a browser."
type: docs
weight: 240
url: /python-net/aspose.words.saving/pdfsaveoptions/open_hyperlinks_in_new_window/
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


JavaScript actions are prohibited by PDF/A-1 and PDF/A-2 compliance. ``False`` will be used automatically when
saving to PDF/A-1 and PDF/A-2.




### Examples

Shows how to save hyperlinks in a document we convert to PDF so that they open new pages when we click on them.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_hyperlink('Testlink', 'https://www.google.com/search?q=%20aspose', False)
# Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()
# Set the "OpenHyperlinksInNewWindow" property to "true" to save all hyperlinks using Javascript code
# that forces readers to open these links in new windows/browser tabs.
# Set the "OpenHyperlinksInNewWindow" property to "false" to save all hyperlinks normally.
options.open_hyperlinks_in_new_window = open_hyperlinks_in_new_window
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.OpenHyperlinksInNewWindow.pdf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

