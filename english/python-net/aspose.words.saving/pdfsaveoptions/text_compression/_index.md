---
title: text_compression property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies compression type to be used for all textual content in the document."
type: docs
weight: 290
url: /python-net/aspose.words.saving/pdfsaveoptions/text_compression/
---

## PdfSaveOptions.text_compression property

Specifies compression type to be used for all textual content in the document.

Default is [PdfTextCompression.FLATE](../../pdftextcompression/#FLATE).

Significantly increases output size when saving a document without compression.




### Examples

Shows how to apply text compression when saving a document to PDF.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

for i in range(100):
    builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

# Create a "PdfSaveOptions" object that we can pass to the document's "save" method
# to modify how that method converts the document to .PDF.
options = aw.saving.PdfSaveOptions()

# Set the "text_compression" property to "PdfTextCompression.NONE" to not apply any
# compression to text when we save the document to PDF.
# Set the "text_compression" property to "PdfTextCompression.FLATE" to apply ZIP compression
# to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
options.text_compression = pdf_text_compression

doc.save(ARTIFACTS_DIR + "PdfSaveOptions.text_compression.pdf", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PdfSaveOptions](../)

