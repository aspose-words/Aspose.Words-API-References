﻿---
title: FontInfo class
linktitle: FontInfo class
articleTitle: FontInfo class
second_title: Aspose.Words for Python
description: "aspose.words.fonts.FontInfo class. Specifies information about a font used in the document"
type: docs
weight: 90
url: /python-net/aspose.words.fonts/fontinfo/
---

## FontInfo class

Specifies information about a font used in the document.
To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/python-net/working-with-fonts/) documentation article.




You do not create instances of this class directly. 
Use the [DocumentBase.font_infos](../../aspose.words/documentbase/font_infos/) property to access the collection of fonts 
defined in a document.




### Properties

| Name | Description |
| --- | --- |
| [alt_name](./alt_name/) | Gets or sets the alternate name for the font. |
| [charset](./charset/) | Gets or sets the character set for the font. |
| [family](./family/) | Gets or sets the font family this font belongs to. |
| [is_true_type](./is_true_type/) | Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is ``True``. |
| [name](./name/) | Gets the name of the font. |
| [panose](./panose/) | Gets or sets the PANOSE typeface classification number. |
| [pitch](./pitch/) | The pitch indicates if the font is fixed pitch, proportionally spaced, or relies on a default setting. |

### Methods

| Name | Description |
| --- | --- |
|[ get_embedded_font(format, style)](./get_embedded_font/#embeddedfontformat_embeddedfontstyle) | Gets a specific embedded font file. |
|[ get_embedded_font_as_open_type(style)](./get_embedded_font_as_open_type/#embeddedfontstyle) | Gets an embedded font file in OpenType format. Fonts in Embedded OpenType format are converted to OpenType. |

### Examples

Shows how to print the details of what fonts are present in a document.

```python
doc = aw.Document(MY_DIR + "Embedded font.docx")

all_fonts = doc.font_infos

# Print all the used and unused fonts in the document.
for i in range(all_fonts.count):
    print(f"Font index #{i}")
    print(f"\tName: {all_fonts[i].name}")
    print(f'\tIs {"" if all_fonts[i].is_true_type else "not "}a TrueType font')
```

### See Also

* module [aspose.words.fonts](../)
* class [FontInfoCollection](../fontinfocollection/)
* property [DocumentBase.font_infos](../../aspose.words/documentbase/font_infos/)

