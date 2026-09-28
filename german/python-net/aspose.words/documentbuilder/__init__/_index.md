---
title: DocumentBuilder constructor
linktitle: DocumentBuilder constructor
articleTitle: DocumentBuilder constructor
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder constructor"
type: docs
weight: 10
url: /de/python-net/aspose.words/documentbuilder/__init__/
---

## DocumentBuilder() {#default}

Initializes a new instance of this class.


```python
def __init__(self):
    ...
```

### Remarks

Creates a new [DocumentBuilder](../) object and attaches it to a new [Document](../../document/) object.



## DocumentBuilder(options) {#documentbuilderoptions}

Initializes a new instance of this class.


```python
def __init__(self, options: aspose.words.DocumentBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| options | [DocumentBuilderOptions](../../documentbuilderoptions/) |  |

### Remarks

Creates a new [DocumentBuilder](../) object and attaches it to a new [Document](../../document/) object.
Additional document building options can be specified.



## DocumentBuilder(doc) {#document}

Initializes a new instance of this class.


```python
def __init__(self, doc: aspose.words.Document):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../document/) | The [Document](../../document/) object to attach to. |

### Remarks

Creates a new [DocumentBuilder](../) object, attaches to the specified [Document](../../document/) object.
The cursor is positioned at the beginning of the document.



## DocumentBuilder(doc, options) {#document_documentbuilderoptions}

Initializes a new instance of this class.


```python
def __init__(self, doc: aspose.words.Document, options: aspose.words.DocumentBuilderOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [Document](../../document/) | The [Document](../../document/) object to attach to. |
| options | [DocumentBuilderOptions](../../documentbuilderoptions/) | Additional options for the document building process. |

### Remarks

Creates a new [DocumentBuilder](../) object, attaches to the specified [Document](../../document/) object.
The cursor is positioned at the beginning of the document.



## Examples

Shows how to ignore table formatting for content after.

```python
doc = aw.Document()
builder_options = aw.DocumentBuilderOptions()
builder_options.context_table_formatting = True
builder = aw.DocumentBuilder(doc=doc, options=builder_options)
# Fügt Inhalt vor der Tabelle hinzu.
# Die Standardschriftgröße beträgt 12.
builder.writeln('Font size 12 here.')
builder.start_table()
builder.insert_cell()
# Ändert die Schriftgröße innerhalb der Tabelle.
builder.font.size = 5
builder.write('Font size 5 here')
builder.insert_cell()
builder.write('Font size 5 here')
builder.end_row()
builder.end_table()
# Wenn ContextTableFormatting true ist, wird die Tabellenformatierung nicht auf den nachfolgenden Inhalt angewendet.
# Wenn ContextTableFormatting false ist, wird die Tabellenformatierung auf den nachfolgenden Inhalt angewendet.
builder.writeln('Font size 12 here.')
doc.save(file_name=ARTIFACTS_DIR + 'Table.ContextTableFormatting.docx')
```

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

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

