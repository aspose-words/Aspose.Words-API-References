---
title: ParagraphFormat.style_identifier property
linktitle: style_identifier property
articleTitle: style_identifier property
second_title: Aspose.Words for Python
description: "ParagraphFormat.style_identifier property. Gets or sets the locale independent style identifier of the paragraph style applied to this formatting."
type: docs
weight: 360
url: /de/python-net/aspose.words/paragraphformat/style_identifier/
---

## ParagraphFormat.style_identifier property

Gets or sets the locale independent style identifier of the paragraph style applied to this formatting.


```python
@property
def style_identifier(self) -> aspose.words.StyleIdentifier:
    ...

@style_identifier.setter
def style_identifier(self, value: aspose.words.StyleIdentifier):
    ...

```

### Examples

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

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

