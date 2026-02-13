---
title: PageSetup class
linktitle: PageSetup class
articleTitle: PageSetup class
second_title: Aspose.Words for Python
description: "aspose.words.PageSetup class. Represents the page setup properties of a section"
type: docs
weight: 920
url: /python-net/aspose.words/pagesetup/
---

## PageSetup class

Represents the page setup properties of a section.
To learn more, visit the [Working with Sections](https://docs.aspose.com/words/python-net/working-with-sections/) documentation article.




### Remarks

[PageSetup](./) object contains all the page setup attributes of a section
(left margin, bottom margin, paper size, and so on) as properties.




### Properties

| Name | Description |
| --- | --- |
| [bidi](./bidi/) | Specifies that this section contains bidirectional (complex scripts) text. |
| [border_always_in_front](./border_always_in_front/) | Specifies where the page border is positioned relative to intersecting texts and objects. |
| [border_applies_to](./border_applies_to/) | Specifies which pages the page border is printed on. |
| [border_distance_from](./border_distance_from/) | Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds. |
| [border_surrounds_footer](./border_surrounds_footer/) | Specifies whether the page border includes or excludes the footer. |
| [border_surrounds_header](./border_surrounds_header/) | Specifies whether the page border includes or excludes the header. |
| [borders](./borders/) | Gets a collection of the page borders. |
| [bottom_margin](./bottom_margin/) | Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text. |
| [chapter_page_separator](./chapter_page_separator/) | Gets or sets the separator character that appears between the chapter number and the page number. |
| [characters_per_line](./characters_per_line/) | Gets or sets the number of characters per line in the document grid. |
| [different_first_page_header_footer](./different_first_page_header_footer/) | True if a different header or footer is used on the first page. |
| [endnote_options](./endnote_options/) | Provides options that control numbering and positioning of endnotes in this section. |
| [first_page_tray](./first_page_tray/) | Gets or sets the paper tray (bin) to use for the first page of a section. The value is implementation (printer) specific. |
| [footer_distance](./footer_distance/) | Returns or sets the distance (in points) between the footer and the bottom of the page. |
| [footnote_options](./footnote_options/) | Provides options that control numbering and positioning of footnotes in this section. |
| [gutter](./gutter/) | Gets or sets the amount of extra space added to the margin for document binding. |
| [header_distance](./header_distance/) | Returns or sets the distance (in points) between the header and the top of the page. |
| [heading_level_for_chapter](./heading_level_for_chapter/) | Gets or sets the heading level style that is applied to the chapter titles in the document. |
| [layout_mode](./layout_mode/) | Gets or sets the layout mode of this section. |
| [left_margin](./left_margin/) | Returns or sets the distance (in points) between the left edge of the page and the left boundary of the body text. |
| [line_number_count_by](./line_number_count_by/) | Returns or sets the numeric increment for line numbers. |
| [line_number_distance_from_text](./line_number_distance_from_text/) | Gets or sets distance between the right edge of line numbers and the left edge of the document. |
| [line_number_restart_mode](./line_number_restart_mode/) | Gets or sets the way line numbering runs  that is, whether it starts over at the beginning of a new page or section or runs continuously. |
| [line_starting_number](./line_starting_number/) | Gets or sets the starting line number. |
| [lines_per_page](./lines_per_page/) | Gets or sets the number of lines per page in the document grid. |
| [margins](./margins/) | Returns or sets preset [Margins](../margins/) of the page. |
| [multiple_pages](./multiple_pages/) | For multiple page documents, gets or sets how a document is printed or rendered so that it can be bound as a booklet. |
| [odd_and_even_pages_header_footer](./odd_and_even_pages_header_footer/) | True if the document has different headers and footers for odd-numbered and even-numbered pages. |
| [orientation](./orientation/) | Returns or sets the orientation of the page. |
| [other_pages_tray](./other_pages_tray/) | Gets or sets the paper tray (bin) to be used for all but the first page of a section. The value is implementation (printer) specific. |
| [page_height](./page_height/) | Returns or sets the height of the page in points. |
| [page_number_style](./page_number_style/) | Gets or sets the page number format. |
| [page_starting_number](./page_starting_number/) | Gets or sets the starting page number of the section. |
| [page_width](./page_width/) | Returns or sets the width of the page in points. |
| [paper_size](./paper_size/) | Returns or sets the paper size. |
| [restart_page_numbering](./restart_page_numbering/) | True if page numbering restarts at the beginning of the section. |
| [right_margin](./right_margin/) | Returns or sets the distance (in points) between the right edge of the page and the right boundary of the body text. |
| [rtl_gutter](./rtl_gutter/) | Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language. |
| [section_start](./section_start/) | Returns or sets the type of section break for the specified object. |
| [sheets_per_booklet](./sheets_per_booklet/) | Returns or sets the number of pages to be included in each booklet. |
| [suppress_endnotes](./suppress_endnotes/) | True if endnotes are printed at the end of the next section that doesn't suppress endnotes. Suppressed endnotes are printed before the endnotes in that section. |
| [text_columns](./text_columns/) | Returns a collection that represents the set of text columns. |
| [text_orientation](./text_orientation/) | Allows to specify [PageSetup.text_orientation](./text_orientation/) for the whole page. Default value is [TextOrientation.HORIZONTAL](../textorientation/#HORIZONTAL) |
| [top_margin](./top_margin/) | Returns or sets the distance (in points) between the top edge of the page and the top boundary of the body text. |
| [vertical_alignment](./vertical_alignment/) | Returns or sets the vertical alignment of text on each page in a document or section. |

### Methods

| Name | Description |
| --- | --- |
|[ clear_formatting()](./clear_formatting/#default) | Resets page setup to default paper size, margins and orientation. |

### Examples

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Modify the page setup properties for the builder's current section and add text.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# If we start a new section using a document builder,
# it will inherit the builder's current page setup properties.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# We can revert its page setup properties to their default values using the "ClearFormatting" method.
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../)

