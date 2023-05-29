---
title: HtmlSaveOptions.export_font_resources property
linktitle: export_font_resources property
articleTitle: export_font_resources property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.export_font_resources property. Specifies whether font resources should be exported to HTML, MHTML or EPUB"
type: docs
weight: 150
url: /python-net/aspose.words.saving/htmlsaveoptions/export_font_resources/
---

## HtmlSaveOptions.export_font_resources property

Specifies whether font resources should be exported to HTML, MHTML or EPUB.
Default is ``False``.


Exporting font resources allows for consistent document rendering independent of the fonts available
in a given user's environment.

If [HtmlSaveOptions.export_font_resources](./) is set to ``True``, main HTML document will refer to every font via 
the CSS 3 **@font-face** at-rule and fonts will be output as separate files. When exporting to IDPF EPUB or MHTML 
formats, fonts will be embedded into the corresponding package along with other subsidiary files.

If [HtmlSaveOptions.export_fonts_as_base64](../export_fonts_as_base64/) is set to ``True``, fonts will not be saved to separate files.
Instead, they will be embedded into **@font-face** at-rules in Base64 encoding.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable
font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not
allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules
in CSS style sheets is not allowed. Font subsetting can also violate license terms.





### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.font_resources_subsetting_size_threshold](../font_resources_subsetting_size_threshold/)

