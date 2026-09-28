---
title: ListLevel.number_style property
linktitle: number_style property
articleTitle: number_style property
second_title: Aspose.Words for Python
description: "ListLevel.number_style property. Returns or sets the number style for this list level."
type: docs
weight: 90
url: /de/python-net/aspose.words.lists/listlevel/number_style/
---

## ListLevel.number_style property

Returns or sets the number style for this list level.


```python
@property
def number_style(self) -> aspose.words.NumberStyle:
    ...

@number_style.setter
def number_style(self, value: aspose.words.NumberStyle):
    ...

```

### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()
# Eine Liste ermöglicht es uns, Satzgruppen von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
# Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
# Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
# Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste hinzufügen, wird zu einem Element der Liste.
# Erstellen Sie eine Liste aus einer Microsoft‑Word-Vorlage und passen Sie die ersten beiden Listenebenen an.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
list_level = doc_list.list_levels[0]
list_level.font.color = aspose.pydrawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = '\x00'
list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144
list_level = doc_list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = 'Wingdings'
list_level.font.color = aspose.pydrawing.Color.blue
list_level.font.size = 24
# Dieser NumberFormat‑Wert erzeugt sternförmige Aufzählungssymbole.
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# Erstellen Sie Absätze und wenden Sie beide Listenebenen unserer benutzerdefinierten Listformatierung darauf an.
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.list = doc_list
builder.writeln('The quick brown fox...')
builder.writeln('The quick brown fox...')
builder.list_format.list_indent()
builder.writeln('jumped over the lazy dog.')
builder.writeln('jumped over the lazy dog.')
builder.list_format.list_outdent()
builder.writeln('The quick brown fox...')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateCustomList.docx')
```

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

