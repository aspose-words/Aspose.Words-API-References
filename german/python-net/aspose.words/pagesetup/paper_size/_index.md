---
title: PageSetup.paper_size property
linktitle: paper_size property
articleTitle: paper_size property
second_title: Aspose.Words for Python
description: "PageSetup.paper_size property. Returns or sets the paper size."
type: docs
weight: 350
url: /de/python-net/aspose.words/pagesetup/paper_size/
---

## PageSetup.paper_size property

Returns or sets the paper size.


```python
@property
def paper_size(self) -> aspose.words.PaperSize:
    ...

@paper_size.setter
def paper_size(self, value: aspose.words.PaperSize):
    ...

```

### Remarks

Setting this property updates [PageSetup.page_width](../page_width/) and [PageSetup.page_height](../page_height/) values.
Setting this value to [PaperSize.CUSTOM](../../papersize/#CUSTOM) does not change existing values.




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

Shows how to set the paper size of JisB4 or JisB5.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
page_setup = doc.first_section.page_setup
# Setzen Sie die Papiergröße auf JisB4 (257x364mm).
page_setup.paper_size = aw.PaperSize.JIS_B4
# Alternativ setzen Sie die Papiergröße auf JisB5. (182x257mm).
page_setup.paper_size = aw.PaperSize.JIS_B5
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

* module [aspose.words](../../)
* class [PageSetup](../)

