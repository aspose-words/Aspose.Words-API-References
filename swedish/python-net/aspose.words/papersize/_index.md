---
title: PaperSize enumeration
linktitle: PaperSize enumeration
articleTitle: PaperSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.PaperSize enumeration. Specifies paper size."
type: docs
weight: 950
url: /sv/python-net/aspose.words/papersize/
---

## PaperSize enumeration

Specifies paper size.


### Members

| Name | Description |
| --- | --- |
| A3 | 297 x 420 mm. |
| A4 | 210 x 297 mm. |
| A5 | 148 x 210 mm. |
| B4 | 250 x 353 mm. |
| B5 | 176 x 250 mm. |
| EXECUTIVE | 7.25 x 10.5 inches. |
| FOLIO | 8.5 x 13 inches. |
| LEDGER | 17 x 11 inches. |
| LEGAL | 8.5 x 14 inches. |
| LETTER | 8.5 x 11 inches. |
| ENVELOPE_DL | 110 x 220 mm. |
| QUARTO | 8.47 x 10.83 inches. |
| STATEMENT | 8.5 x 5.5 inches. |
| TABLOID | 11 x 17 inches. |
| PAPER_10X14 | 10 x 14 inches. |
| PAPER_11X17 | 11 x 17 inches. |
| NUMBER_10_ENVELOPE | 4.125 x 9.5 inches. |
| JIS_B4 | 257 x 364 mm. |
| JIS_B5 | 182 x 257 mm. |
| CUSTOM | Custom paper size. |

### Examples

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.page_setup.paper_size = aw.PaperSize.LEGAL
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.top_margin = aw.ConvertUtil.inch_to_point(1)
builder.page_setup.bottom_margin = aw.ConvertUtil.inch_to_point(1)
builder.page_setup.left_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.right_margin = aw.ConvertUtil.inch_to_point(1.5)
builder.page_setup.header_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.page_setup.footer_distance = aw.ConvertUtil.inch_to_point(0.2)
builder.writeln('Hello world!')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageMargins.docx')
```

Shows how to set page sizes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Vi kan ändra den aktuella sidans storlek till en fördefinierad storlek
# genom att använda egenskapen "PaperSize" i detta avsnitts PageSetup-objekt.
builder.page_setup.paper_size = aw.PaperSize.TABLOID
self.assertEqual(792, builder.page_setup.page_width)
self.assertEqual(1224, builder.page_setup.page_height)
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
# Varje avsnitt har sitt eget PageSetup-objekt. När vi använder en dokumentbyggare för att skapa ett nytt avsnitt,
# ärver det avsnittets PageSetup-objekt alla värden från föregående avsnitts PageSetup-objekt.
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
self.assertEqual(aw.PaperSize.TABLOID, builder.page_setup.paper_size)
builder.page_setup.paper_size = aw.PaperSize.A5
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
self.assertEqual(419.55, builder.page_setup.page_width)
self.assertEqual(595.3, builder.page_setup.page_height)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
# Ställ in en anpassad storlek för detta avsnitts sidor.
builder.page_setup.page_width = 620
builder.page_setup.page_height = 480
self.assertEqual(aw.PaperSize.CUSTOM, builder.page_setup.paper_size)
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PaperSizes.docx')
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Ett tomt dokument innehåller en sektion, en kropp och ett stycke.
# Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
# och sluta med ett dokumentnod utan några barn.
doc.remove_all_children()
# Detta dokument har nu inga sammansatta barnnoder som vi kan lägga till innehåll i.
# Om vi vill redigera det måste vi återfylla dess nodsamling.
# Först, skapa en ny sektion och lägg sedan till den som ett barn till rot-dokumentnoden.
section = aw.Section(doc)
doc.append_child(section)
# Ställ in några sidinställningsegenskaper för sektionen.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# En sektion behöver en kropp, som kommer att innehålla och visa allt dess innehåll
# på sidan mellan sektionens sidhuvud och sidfot.
body = aw.Body(doc)
section.append_child(body)
# Skapa ett stycke, ställ in några formateringsegenskaper och lägg sedan till det som ett barn till kroppen.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Slutligen, lägg till lite innehåll i dokumentet. Skapa en run,
# ställ in dess utseende och innehåll, och lägg sedan till den som ett barn till stycket.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../)

