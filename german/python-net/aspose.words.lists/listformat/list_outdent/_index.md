---
title: ListFormat.list_outdent method
linktitle: list_outdent method
articleTitle: list_outdent method
second_title: Aspose.Words for Python
description: "ListFormat.list_outdent method. Decreases the list level of the current paragraph by one level."
type: docs
weight: 80
url: /de/python-net/aspose.words.lists/listformat/list_outdent/
---

## list_outdent() {#default}

Decreases the list level of the current paragraph by one level.


```python
def list_outdent(self):
    ...
```

### Remarks

This method changes the list level and applies formatting properties of the new level.

In Word documents, lists may consist of up to nine levels. List formatting
for each level specifies what bullet or number is used, left indent, space between
the bullet and text etc.




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

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

