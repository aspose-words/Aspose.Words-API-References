---
title: Document.last_section property
linktitle: last_section property
articleTitle: last_section property
second_title: Aspose.Words for Python
description: "Document.last_section property. Gets the last section in the document."
type: docs
weight: 250
url: /de/python-net/aspose.words/document/last_section/
---

## Document.last_section property

Gets the last section in the document.


```python
@property
def last_section(self) -> aspose.words.Section:
    ...

```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to create a new section with a document builder.

```python
doc = aw.Document()
# Ein leeres Dokument enthält standardmäßig einen Abschnitt,
# der Kindknoten enthält, die wir bearbeiten können.
self.assertEqual(1, doc.sections.count)
# Verwenden Sie einen DocumentBuilder, um Text zum ersten Abschnitt hinzuzufügen.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Erstellen Sie einen zweiten Abschnitt, indem Sie einen Abschnittsumbruch einfügen.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(2, doc.sections.count)
# Jeder Abschnitt hat eigene Seiteneinrichtungs‑Einstellungen.
# Wir können den Text im zweiten Abschnitt in zwei Spalten aufteilen.
# Dies wirkt sich nicht auf den Text im ersten Abschnitt aus.
doc.last_section.page_setup.text_columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
self.assertEqual(1, doc.first_section.page_setup.text_columns.count)
self.assertEqual(2, doc.last_section.page_setup.text_columns.count)
doc.save(file_name=ARTIFACTS_DIR + 'Section.Create.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

