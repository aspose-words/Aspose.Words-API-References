---
title: ViewOptions.do_not_display_page_boundaries property
linktitle: do_not_display_page_boundaries property
articleTitle: do_not_display_page_boundaries property
second_title: Aspose.Words for Python
description: "ViewOptions.do_not_display_page_boundaries property. Turns off display of the space between the top of the text and the top edge of the page."
type: docs
weight: 20
url: /de/python-net/aspose.words.settings/viewoptions/do_not_display_page_boundaries/
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
# Fügen Sie Inhalt ein, der sich über 3 Seiten erstreckt.
builder.writeln('Paragraph 1, Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Paragraph 2, Page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Paragraph 3, Page 3.')
# Fügen Sie eine Kopfzeile und eine Fußzeile ein.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln('This is the header.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln('This is the footer.')
# Dieses Dokument enthält eine kleine Menge an Inhalt, die ein paar ganze Seiten einnimmt.
# Setzen Sie das "DoNotDisplayPageBoundaries"-Flag auf "true", um ältere Versionen von Microsoft Word dazu zu bringen, Kopfzeilen zu unterdrücken,
# Fußzeilen und einen Großteil des vertikalen Leerraums beim Anzeigen unseres Dokuments.
# Setzen Sie das "DoNotDisplayPageBoundaries"-Flag auf "false", um ältere Versionen von Microsoft Word
# zur normalen Anzeige unseres Dokuments.
doc.view_options.do_not_display_page_boundaries = do_not_display_page_boundaries
doc.save(file_name=ARTIFACTS_DIR + 'ViewOptions.DisplayPageBoundaries.doc')
```

### See Also

* module [aspose.words.settings](../../)
* class [ViewOptions](../)

