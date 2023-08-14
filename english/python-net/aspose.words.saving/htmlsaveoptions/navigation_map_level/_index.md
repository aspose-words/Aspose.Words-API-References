---
title: HtmlSaveOptions.navigation_map_level property
linktitle: navigation_map_level property
articleTitle: navigation_map_level property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.navigation_map_level property. Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3 formats"
type: docs
weight: 400
url: /python-net/aspose.words.saving/htmlsaveoptions/navigation_map_level/
---

## HtmlSaveOptions.navigation_map_level property

Specifies the maximum level of headings populated to the navigation map when exporting to EPUB, MOBI, or AZW3
formats. Default value is ``3``.


The navigation map allows user agents to provide an easy way of navigation through the document structure.
Usually navigation points correspond to headings in the document. In order to populate headings up to level **N**
assign this value to [HtmlSaveOptions.navigation_map_level](./).

By default, three levels of headings are populated: paragraphs of styles **Heading 1**, **Heading 2**
and **Heading 3**.
You can set this property to a value from 1 to 9 in order to request the corresponding maximum level.
Setting it to zero will reduce the navigation map to only the document root or roots of document parts.




### Examples

Shows how to generate table of contents for Mobi documents.

```python
doc = aw.Document(MY_DIR + "Big document.docx")

options = aw.saving.HtmlSaveOptions(aw.SaveFormat.MOBI)
options.navigation_map_level = 5

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.CreateMobiToc.mobi", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)

