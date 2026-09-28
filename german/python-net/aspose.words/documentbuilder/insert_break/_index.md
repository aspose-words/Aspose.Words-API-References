---
title: DocumentBuilder.insert_break method
linktitle: insert_break method
articleTitle: insert_break method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_break method. Inserts a break of the specified type into the document."
type: docs
weight: 260
url: /de/python-net/aspose.words/documentbuilder/insert_break/
---

## insert_break(break_type) {#breaktype}

Inserts a break of the specified type into the document.


```python
def insert_break(self, break_type: aspose.words.BreakType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| break_type | [BreakType](../../breaktype/) | Specifies the type of the break to insert. |

### Remarks

Use this method to insert paragraph, page, column, section or line break into the document.


### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Geben Sie an, dass wir unterschiedliche Kopf- und Fußzeilen für die erste, gerade und ungerade Seiten wünschen.
builder.page_setup.different_first_page_header_footer = True
builder.page_setup.odd_and_even_pages_header_footer = True
# Erstellen Sie die Kopfzeilen und fügen Sie dann dem Dokument drei Seiten hinzu, um jeden Kopfzeilentyp anzuzeigen.
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_FIRST)
builder.write('Header for the first page')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_EVEN)
builder.write('Header for even pages')
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('Header for all other pages')
builder.move_to_section(0)
builder.writeln('Page1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page3')
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.HeadersAndFooters.docx')
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Fügen Sie ein Inhaltsverzeichnis für die erste Seite des Dokuments ein.
# Konfigurieren Sie das Verzeichnis so, dass es Absätze mit Überschriften der Ebenen 1 bis 3 übernimmt.
# Stellen Sie außerdem ein, dass seine Einträge Hyperlinks sind, die uns führen
# zur Position der Überschrift, wenn in Microsoft Word linksgeklickt wird.
builder.insert_table_of_contents('\\o "1-3" \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Füllen Sie das Inhaltsverzeichnis, indem Sie Absätze mit Überschriftstilen hinzufügen.
# Jede solche Überschrift mit einer Ebene zwischen 1 und 3 erzeugt einen Eintrag in der Tabelle.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 1.1')
builder.writeln('Heading 1.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Heading 2')
builder.writeln('Heading 3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.1')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING3
builder.writeln('Heading 3.1.1')
builder.writeln('Heading 3.1.2')
builder.writeln('Heading 3.1.3')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING4
builder.writeln('Heading 3.1.3.1')
builder.writeln('Heading 3.1.3.2')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING2
builder.writeln('Heading 3.2')
builder.writeln('Heading 3.3')
# Ein Inhaltsverzeichnis ist ein Feld eines Typs, das aktualisiert werden muss, um ein aktuelles Ergebnis anzuzeigen.
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertToc.docx')
```

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ändern Sie die Seiteneinrichtungseigenschaften für den aktuellen Abschnitt des Builders und fügen Sie Text hinzu.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# Wenn wir einen neuen Abschnitt mit einem Document Builder starten,
# erbt er die aktuellen Seiteneinrichtungseigenschaften des Builders.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# Wir können seine Seiteneinrichtungseigenschaften mit der Methode "ClearFormatting" auf ihre Standardwerte zurücksetzen.
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

