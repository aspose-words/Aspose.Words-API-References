---
title: PaperSize enumeration
linktitle: PaperSize enumeration
articleTitle: PaperSize enumeration
second_title: Aspose.Words for Python
description: "aspose.words.PaperSize enumeration. Specifies paper size."
type: docs
weight: 950
url: /de/python-net/aspose.words/papersize/
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
# Wir können die Größe der aktuellen Seite auf eine vordefinierte Größe ändern
# indem wir die Eigenschaft "PaperSize" des PageSetup-Objekts dieses Abschnitts verwenden.
builder.page_setup.paper_size = aw.PaperSize.TABLOID
self.assertEqual(792, builder.page_setup.page_width)
self.assertEqual(1224, builder.page_setup.page_height)
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
# Jeder Abschnitt hat sein eigenes PageSetup-Objekt. Wenn wir einen DocumentBuilder verwenden, um einen neuen Abschnitt zu erstellen,
# erbt das PageSetup-Objekt dieses Abschnitts alle Werte des PageSetup-Objekts des vorherigen Abschnitts.
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
self.assertEqual(aw.PaperSize.TABLOID, builder.page_setup.paper_size)
builder.page_setup.paper_size = aw.PaperSize.A5
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
self.assertEqual(419.55, builder.page_setup.page_width)
self.assertEqual(595.3, builder.page_setup.page_height)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
# Eine benutzerdefinierte Größe für die Seiten dieses Abschnitts festlegen.
builder.page_setup.page_width = 620
builder.page_setup.page_height = 480
self.assertEqual(aw.PaperSize.CUSTOM, builder.page_setup.paper_size)
builder.writeln(f'This page is {builder.page_setup.page_width}x{builder.page_setup.page_height}.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PaperSizes.docx')
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Ein leeres Dokument enthält einen Abschnitt, einen Body und einen Absatz.
# Rufen Sie die \"RemoveAllChildren\"-Methode auf, um alle diese Knoten zu entfernen,
# und erhalten einen Dokumentknoten ohne Kinder.
doc.remove_all_children()
# Dieses Dokument hat jetzt keine zusammengesetzten Kindknoten, zu denen wir Inhalte hinzufügen können.
# Wenn wir es bearbeiten möchten, müssen wir seine Knotensammlung neu befüllen.
# Zuerst erstellen Sie einen neuen Abschnitt und fügen ihn dann als Kind zum Wurzel-Dokumentknoten hinzu.
section = aw.Section(doc)
doc.append_child(section)
# Legen Sie einige Seiteneinrichtungs‑Eigenschaften für den Abschnitt fest.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Ein Abschnitt benötigt einen Body, der alle seine Inhalte enthält und anzeigt
# auf der Seite zwischen dem Header und Footer des Abschnitts.
body = aw.Body(doc)
section.append_child(body)
# Erstellen Sie einen Absatz, setzen Sie einige Formatierungseigenschaften und fügen Sie ihn dann als Kind zum Body hinzu.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Schließlich fügen Sie etwas Inhalt zum Dokument hinzu. Erstellen Sie einen Run,
# setzen Sie sein Aussehen und seinen Inhalt und fügen Sie ihn dann als Kind zum Absatz hinzu.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../)

