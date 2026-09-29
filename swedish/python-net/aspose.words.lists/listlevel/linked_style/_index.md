---
title: ListLevel.linked_style property
linktitle: linked_style property
articleTitle: linked_style property
second_title: Aspose.Words for Python
description: "ListLevel.linked_style property. Gets or sets the paragraph style that is linked to this list level."
type: docs
weight: 60
url: /sv/python-net/aspose.words.lists/listlevel/linked_style/
---

## ListLevel.linked_style property

Gets or sets the paragraph style that is linked to this list level.


```python
@property
def linked_style(self) -> aspose.words.Style:
    ...

@linked_style.setter
def linked_style(self, value: aspose.words.Style):
    ...

```

### Remarks

This property is ``None`` when the list level is not linked to a paragraph style.
This property can be set to ``None``.




### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
# Vi kan skapa nästlade listor genom att öka indragnivån.
# Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
# Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# Etiketter på nivå 1 kommer att formateras enligt styckeformatet "Heading 1" och kommer att ha ett prefix.
# Dessa kommer att se ut som "Appendix A", "Appendix B"...
doc_list.list_levels[0].number_format = 'Appendix \x00'
doc_list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
doc_list.list_levels[0].linked_style = doc.styles.get_by_name('Heading 1')
# Etiketter på nivå 2 kommer att visa de aktuella siffrorna för den första och den andra listnivån och ha inledande nollor.
# Om den första listnivån är 1, kommer listetiketterna från dessa att se ut som "Section (1.01)", "Section (1.02)"...
doc_list.list_levels[1].number_format = 'Section (\x00.\x01)'
doc_list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO
# Observera att den högre nivån använder UppercaseLetter-numrering.
# Vi kan sätta egenskapen "IsLegal" för att använda arabiska siffror för de högre listnivåerna.
doc_list.list_levels[1].is_legal = True
doc_list.list_levels[1].restart_after_level = 0
# Etiketter på nivå 3 kommer att vara stora romerska siffror med ett prefix och ett suffix och startas om för varje List-nivå‑1‑objekt.
# Dessa listetiketter kommer att se ut som "-I-", "-II-"...
doc_list.list_levels[2].number_format = '-\x02-'
doc_list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc_list.list_levels[2].restart_after_level = 1
# Gör etiketter på alla listnivåer fetstil.
for level in doc_list.list_levels:
    level.font.bold = True
# Applicera listformatering på det aktuella stycket.
builder.list_format.list = doc_list
# Skapa listobjekt som visar alla tre av våra listnivåer.
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

