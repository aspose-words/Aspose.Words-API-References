---
title: PageSetup.page_starting_number property
linktitle: page_starting_number property
articleTitle: page_starting_number property
second_title: Aspose.Words for Python
description: "PageSetup.page_starting_number property. Gets or sets the starting page number of the section."
type: docs
weight: 330
url: /de/python-net/aspose.words/pagesetup/page_starting_number/
---

## PageSetup.page_starting_number property

Gets or sets the starting page number of the section.


```python
@property
def page_starting_number(self) -> int:
    ...

@page_starting_number.setter
def page_starting_number(self, value: int):
    ...

```

### Remarks

The [PageSetup.restart_page_numbering](../restart_page_numbering/) property, if set to ``False``, will override the
[PageSetup.page_starting_number](./) property so that page numbering can continue from the previous section.



### Examples

Shows how to set up page numbering in a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Section 1, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 1, page 3.')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('Section 2, page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Section 2, page 3.')
# Verschieben Sie den Document Builder zum primären Header des ersten Abschnitts,
# die jede Seite in diesem Abschnitt anzeigt.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
# Fügen Sie ein PAGE-Feld ein, das die Nummer der aktuellen Seite anzeigt.
builder.write('Page ')
builder.insert_field(field_code='PAGE', field_value='')
# Konfigurieren Sie den Abschnitt so, dass die Seitenzahl, die PAGE-Felder anzeigen, bei 5 beginnt.
# Konfigurieren Sie außerdem alle PAGE-Felder, ihre Seitenzahlen in Großbuchstaben‑Römischen Ziffern anzuzeigen.
page_setup = doc.sections[0].page_setup
page_setup.restart_page_numbering = True
page_setup.page_starting_number = 5
page_setup.page_number_style = aw.NumberStyle.UPPERCASE_ROMAN
# Erstellen Sie einen weiteren primären Header für den zweiten Abschnitt, mit einem weiteren PAGE-Feld.
builder.move_to_section(1)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
builder.write(' - ')
builder.insert_field(field_code='PAGE', field_value='')
builder.write(' - ')
# Konfigurieren Sie den Abschnitt so, dass die Seitenzahl, die PAGE-Felder anzeigen, bei 10 beginnt.
# Konfigurieren Sie außerdem alle PAGE-Felder, ihre Seitenzahlen mit arabischen Ziffern anzuzeigen.
page_setup = doc.sections[1].page_setup
page_setup.page_starting_number = 10
page_setup.restart_page_numbering = True
page_setup.page_number_style = aw.NumberStyle.ARABIC
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageNumbering.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

