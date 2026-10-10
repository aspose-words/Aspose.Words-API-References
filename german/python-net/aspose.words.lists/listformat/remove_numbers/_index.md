---
title: ListFormat.remove_numbers method
linktitle: remove_numbers method
articleTitle: remove_numbers method
second_title: Aspose.Words for Python
description: "ListFormat.remove_numbers method. Removes numbers or bullets from the current paragraph and sets list level to zero."
type: docs
weight: 90
url: /de/python-net/aspose.words.lists/listformat/remove_numbers/
---

## remove_numbers() {#default}

Removes numbers or bullets from the current paragraph and sets list level to zero.


```python
def remove_numbers(self):
    ...
```

### Remarks

Calling this method is equivalent to setting the [ListFormat.list](../list/) property to ``None``.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Aspose.Words main advantages are:')
# Eine Liste ermöglicht es uns, Satzgruppen von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
# Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
# Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
# Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste hinzufügen, wird zu einem Element der Liste.
# Unten sind zwei Arten von Listen, die wir mit einem Document Builder erstellen können.
# 1 -  Eine Aufzählungsliste:
# Diese Liste wird vor jedem Absatz einen Einzug und ein Aufzählungssymbol ("•") anwenden.
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# Beende die Aufzählungsliste.
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  Eine nummerierte Liste:
# Nummerierte Listen erzeugen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder.list_format.apply_number_default()
# Dieser Absatz ist das erste Element. Das erste Element einer nummerierten Liste hat ein "1." als Listensymbol.
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# Rufe die Methode "ListIndent" auf, um die aktuelle Listenebene zu erhöhen,
# was eine neue eigenständige Liste mit größerer Einrückung am aktuellen Element der ersten Listenebene startet.
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# Dies sind die ersten drei Listenelemente der zweiten Listenebene, die einen Zähler beibehalten
# unabhängig vom Zähler der ersten Listenebene. Gemäß dem aktuellen Listenformat,
# sie werden die Symbole "a.", "b." und "c." haben.
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# Rufe die Methode "ListOutdent" auf, um zur vorherigen Listenebene zurückzukehren.
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# Diese beiden Absätze werden den Zähler der ersten Listenebene fortsetzen.
# Diese Elemente werden die Symbole "2." und "3." haben
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# Wenn wir die Listenebene auf ein Niveau erhöhen, zu dem wir bereits zuvor Elemente hinzugefügt haben,
# wird die verschachtelte Liste vom vorherigen getrennt sein und ihre Nummerierung beginnt von Anfang an.
# Diese Listenelemente werden die Symbole "a.", "b.", "c.", "d." und "e" haben.
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# Rücken Sie die Listenebene erneut zurück.
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# Beenden Sie die nummerierte Liste.
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

Shows how to remove list formatting from all paragraphs in the main text of a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.apply_number_default()
builder.writeln('Numbered list item 1')
builder.writeln('Numbered list item 2')
builder.writeln('Numbered list item 3')
builder.list_format.remove_numbers()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
self.assertEqual(3, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
for paragraph in paras:
    paragraph = paragraph.as_paragraph()
    paragraph.list_format.remove_numbers()
self.assertEqual(0, len(list(filter(lambda n: n.as_paragraph().list_format.is_list_item, paras))))
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

