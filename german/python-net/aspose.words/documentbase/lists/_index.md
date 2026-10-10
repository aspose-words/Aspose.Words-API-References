---
title: DocumentBase.lists property
linktitle: lists property
articleTitle: lists property
second_title: Aspose.Words for Python
description: "DocumentBase.lists property. Provides access to the list formatting used in the document."
type: docs
weight: 50
url: /de/python-net/aspose.words/documentbase/lists/
---

## DocumentBase.lists property

Provides access to the list formatting used in the document.


```python
@property
def lists(self) -> aspose.words.lists.ListCollection:
    ...

```

### Remarks

For more information see the description of the [ListCollection](../../../aspose.words.lists/listcollection/) class.




### Examples

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

* module [aspose.words](../../)
* class [DocumentBase](../)
* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [List](../../../aspose.words.lists/list/)
* class [ListFormat](../../../aspose.words.lists/listformat/)

