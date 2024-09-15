---
title: PclSaveOptions.add_printer_font method
linktitle: add_printer_font method
articleTitle: add_printer_font method
second_title: Aspose.Words for Python
description: "PclSaveOptions.add_printer_font method. Adds information about font that is uploaded to the printer by manufacturer."
type: docs
weight: 50
url: /python-net/aspose.words.saving/pclsaveoptions/add_printer_font/
---

## add_printer_font(font_full_name, font_pcl_name) {#str_str}

Adds information about font that is uploaded to the printer by manufacturer.


```python
def add_printer_font(self, font_full_name: str, font_pcl_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| font_full_name | str | Full name of the font (e.g. "Times New Roman Bold Italic"). |
| font_pcl_name | str | Name of the font that is used in Pcl document. |

### Remarks

There are 52 fonts that are to be built in any printer according to Pcl specification.
However manufactures can add some other fonts to their devices.


### Examples

Shows how to get a printer to substitute all instances of a specific font with a different font.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.font.name = 'Courier'
builder.write('Hello world!')
save_options = aw.saving.PclSaveOptions()
save_options.add_printer_font('Courier New', 'Courier')
# When printing this document, the printer will use the "Courier New" font
# to access places where our document used the "Courier" font.
doc.save(file_name=ARTIFACTS_DIR + 'PclSaveOptions.AddPrinterFont.pcl', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [PclSaveOptions](../)

