---
title: ListFormat.list_level_number property
linktitle: list_level_number property
articleTitle: list_level_number property
second_title: Aspose.Words for Python
description: "ListFormat.list_level_number property. Gets or sets the list level number (0 to 8) for the paragraph."
type: docs
weight: 40
url: /de/python-net/aspose.words.lists/listformat/list_level_number/
---

## ListFormat.list_level_number property

Gets or sets the list level number (0 to 8) for the paragraph.


```python
@property
def list_level_number(self) -> int:
    ...

@list_level_number.setter
def list_level_number(self, value: int):
    ...

```

### Remarks

In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [ListFormat.list](../list/) property is set to reference a valid list.




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

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# Eine Liste ermöglicht es uns, Satzgruppen von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
# Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
# Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
# Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste hinzufügen, wird zu einem Element der Liste.
# Unten sind zwei Listentypen, die wir mit einem Document Builder erstellen können.
# 1 -  Eine nummerierte Liste:
# Nummerierte Listen erzeugen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# Durch das Setzen der "ListLevelNumber"-Eigenschaft können wir die Listenebene erhöhen
# um eine eigenständige Unterliste beim aktuellen Listenelement zu beginnen.
# Die Microsoft‑Word-Listenvorlage mit dem Namen "NumberDefault" verwendet Zahlen, um Listenebenen für die erste Listenebene zu erstellen.
# Tiefere Listenebenen verwenden Buchstaben und kleinbuchstabige römische Ziffern.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  Eine Aufzählungsliste:
# Diese Liste wird vor jedem Absatz einen Einzug und ein Aufzählungssymbol ("•") anwenden.
# Tiefere Ebenen dieser Liste verwenden unterschiedliche Symbole, wie "■" und "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Wir können die Listformatierung deaktivieren, um nachfolgende Absätze nicht als Listen zu formatieren, indem wir das "List"-Flag zurücksetzen.
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)

