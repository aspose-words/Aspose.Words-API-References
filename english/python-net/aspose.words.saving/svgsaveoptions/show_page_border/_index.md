---
title: SvgSaveOptions.show_page_border property
linktitle: show_page_border property
articleTitle: show_page_border property
second_title: Aspose.Words for Python
description: "SvgSaveOptions.show_page_border property. Controls whether a border is added to the outline of the page"
type: docs
weight: 110
url: /python-net/aspose.words.saving/svgsaveoptions/show_page_border/
---

## SvgSaveOptions.show_page_border property

Controls whether a border is added to the outline of the page.
Default is ``True``.



```python
@property
def show_page_border(self) -> bool:
    ...

@show_page_border.setter
def show_page_border(self, value: bool):
    ...

```

### Examples

Shows how to mimic the properties of images when converting a .docx document to .svg.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
# Configure the SvgSaveOptions object to save with no page borders or selectable text.
options = aw.saving.SvgSaveOptions()
options.fit_to_view_port = True
options.show_page_border = False
options.text_output_mode = aw.saving.SvgTextOutputMode.USE_PLACED_GLYPHS
doc.save(file_name=ARTIFACTS_DIR + 'SvgSaveOptions.SaveLikeImage.svg', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SvgSaveOptions](../)

