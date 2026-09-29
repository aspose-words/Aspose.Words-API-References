---
title: ViewOptions.do_not_display_page_boundaries property
linktitle: do_not_display_page_boundaries property
articleTitle: do_not_display_page_boundaries property
second_title: Aspose.Words for Python
description: "ViewOptions.do_not_display_page_boundaries property. Turns off display of the space between the top of the text and the top edge of the page."
type: docs
weight: 20
url: /tr/python-net/aspose.words.settings/viewoptions/do_not_display_page_boundaries/
---

## ViewOptions.do_not_display_page_boundaries property

Turns off display of the space between the top of the text and the top edge of the page.


```python
@property
def do_not_display_page_boundaries(self) -> bool:
    ...

@do_not_display_page_boundaries.setter
def do_not_display_page_boundaries(self, value: bool):
    ...

```

### Examples

Shows how to hide vertical whitespace and headers/footers in view options.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 3 sayfaya yayılan içerik ekleyin.
builder.writeln('Paragraph 1, Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Paragraph 2, Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Paragraph 3, Page 3.')
# Bir üst bilgi ve bir alt bilgi ekleyin.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('This is the header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('This is the footer.')
# Bu belge, birkaç tam sayfa alanı kaplayan az miktarda içerik içerir.
# "DoNotDisplayPageBoundaries" bayrağını "true" olarak ayarlayın, eski Microsoft Word sürümlerinin başlıkları atlamasını sağlamak için,
# altbilgileri ve belgeyi görüntülerken dikey boşlukların çoğunu.
# "DoNotDisplayPageBoundaries" bayrağını "false" olarak ayarlayın, eski Microsoft Word sürümlerinde
# belgemizi normal şekilde görüntülemek için.
doc.view_options.do_not_display_page_boundaries = do_not_display_page_boundaries
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayPageBoundaries.doc')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

