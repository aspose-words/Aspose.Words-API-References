---
title: Story.last_paragraph property
linktitle: last_paragraph property
articleTitle: last_paragraph property
second_title: Aspose.Words for Python
description: "Story.last_paragraph property. Gets the last paragraph in the story."
type: docs
weight: 20
url: /sv/python-net/aspose.words/story/last_paragraph/
---

## Story.last_paragraph property

Gets the last paragraph in the story.


```python
@property
def last_paragraph(self) -> aspose.words.Paragraph:
    ...

```

### Examples

Shows how to move a DocumentBuilder's cursor position to a specified node.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Run 1. ')
# Dokumentbyggaren har en markör, som fungerar som delen av dokumentet
# där byggaren lägger till nya noder när vi använder dess dokumentkonstruktionsmetoder.
# Denna markör fungerar på samma sätt som Microsoft Words blinkande markör,
# och den hamnar också alltid omedelbart efter varje nod som byggaren just infogat.
# För att lägga till innehåll i en annan del av dokumentet,
# kan vi flytta markören till en annan nod med "MoveTo"-metoden.
builder.move_to(doc.first_section.body.first_paragraph.runs[0])
# Markören är nu framför den nod vi flyttade den till.
# Att lägga till ett andra textstycke kommer att infoga det framför det första textstycket.
builder.writeln('Run 2. ')
self.assertEqual('Run 2. \rRun 1.', doc.get_text().strip())
# Flytta markören till slutet av dokumentet för att fortsätta lägga till text i slutet som tidigare.
builder.move_to(doc.last_section.body.last_paragraph)
builder.writeln('Run 3. ')
self.assertEqual('Run 2. \rRun 1. \rRun 3.', doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Story](../)

