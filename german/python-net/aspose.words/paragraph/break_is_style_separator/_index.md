---
title: Paragraph.break_is_style_separator property
linktitle: break_is_style_separator property
articleTitle: break_is_style_separator property
second_title: Aspose.Words for Python
description: "Paragraph.break_is_style_separator property. True if this paragraph break is a Style Separator"
type: docs
weight: 20
url: /de/python-net/aspose.words/paragraph/break_is_style_separator/
---

## Paragraph.break_is_style_separator property

True if this paragraph break is a Style Separator. A style separator allows one
paragraph to consist of parts that have different paragraph styles.


```python
@property
def break_is_style_separator(self) -> bool:
    ...

```

### Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_table_of_contents('\\o \\h \\z \\u')
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Fügen Sie einen Absatz mit einem Stil ein, den das Inhaltsverzeichnis (TOC) als Eintrag übernimmt.
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
# Beide Zeichenketten befinden sich im selben Absatz und werden daher im selben TOC‑Eintrag angezeigt.
builder.write('Heading 1. ')
builder.write('Will appear in the TOC. ')
# Wenn wir einen Stiltrennzeichen einfügen, können wir mehr Text im selben Absatz schreiben
# und einen anderen Stil verwenden, ohne im Inhaltsverzeichnis angezeigt zu werden.
# Wenn wir nach dem Trennzeichen einen Überschriftsstil verwenden, können wir mehrere Einträge im Inhaltsverzeichnis aus einer einzigen Textzeile des Dokuments erzeugen.
builder.insert_style_separator()
builder.paragraph_format.style_identifier = aw.StyleIdentifier.QUOTE
builder.write("Won't appear in the TOC. ")
self.assertTrue(doc.first_section.body.first_paragraph.break_is_style_separator)
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.BreakIsStyleSeparator.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

