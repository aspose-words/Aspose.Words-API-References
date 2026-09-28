---
title: ListLevel.is_legal property
linktitle: is_legal property
articleTitle: is_legal property
second_title: Aspose.Words for Python
description: "ListLevel.is_legal property. True if the level turns all inherited numbers to Arabic, false if it preserves their number style."
type: docs
weight: 50
url: /de/python-net/aspose.words.lists/listlevel/is_legal/
---

## ListLevel.is_legal property

True if the level turns all inherited numbers to Arabic, false if it preserves their number style.


```python
@property
def is_legal(self) -> bool:
    ...

@is_legal.setter
def is_legal(self, value: bool):
    ...

```

### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Eine Liste ermöglicht es uns, Satzgruppen von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
# Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
# Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
# Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste hinzufügen, wird zu einem Element der Liste.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Level‑1‑Beschriftungen werden gemäß dem Absatzstil "Heading 1" formatiert und erhalten ein Präfix.
# Diese sehen aus wie "Appendix A", "Appendix B"...
doc_list.list_levels[0].number_format = 'Appendix \x00'
doc_list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
doc_list.list_levels[0].linked_style = doc.styles.get_by_name('Heading 1')
# Level‑2‑Beschriftungen zeigen die aktuellen Zahlen der ersten und zweiten Listenebenen an und haben führende Nullen.
# Wenn die erste Listenebene bei 1 ist, sehen die Listeneinträge etwa so aus: "Section (1.01)", "Section (1.02)"...
doc_list.list_levels[1].number_format = 'Section (\x00.\x01)'
doc_list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO
# Beachten Sie, dass die höhere Ebene die Nummerierung UppercaseLetter verwendet.
# Wir können die Eigenschaft "IsLegal" setzen, um arabische Zahlen für die höheren Listenebenen zu verwenden.
doc_list.list_levels[1].is_legal = True
doc_list.list_levels[1].restart_after_level = 0
# Level‑3‑Beschriftungen werden große römische Ziffern mit einem Präfix und einem Suffix sein und bei jedem Listeneintrag der Ebene 1 neu beginnen.
# Diese Listeneinträge sehen aus wie "-I-", "-II-"...
doc_list.list_levels[2].number_format = '-\x02-'
doc_list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc_list.list_levels[2].restart_after_level = 1
# Machen Sie die Beschriftungen aller Listenebenen fett.
for level in doc_list.list_levels:
    level.font.bold = True
# Wenden Sie die Listformatierung auf den aktuellen Absatz an.
builder.list_format.list = doc_list
# Erstellen Sie Listenelemente, die alle drei unserer Listenebenen anzeigen.
n = 0
while n < 2:
    i = 0
    while i < 3:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    n += 1
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.CreateListRestartAfterHigher.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

