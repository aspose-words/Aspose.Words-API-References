---
title: ListLevel.number_format property
linktitle: number_format property
articleTitle: number_format property
second_title: Aspose.Words for Python
description: "ListLevel.number_format property. Returns or sets the number format for the list level."
type: docs
weight: 70
url: /sv/python-net/aspose.words.lists/listlevel/number_format/
---

## ListLevel.number_format property

Returns or sets the number format for the list level.


```python
@property
def number_format(self) -> str:
    ...

@number_format.setter
def number_format(self, value: str):
    ...

```

### Remarks

Among normal text characters, the string can contain placeholder characters \\x0000 to \\x0008
representing the numbers from the corresponding list levels.

For example, the string "\\x0000.\\x0001)" will generate a list label
that looks something like "1.5)". The number "1" is the current number from
the 1st list level, the number "5" is the current number from the 2nd list level.

Null is not allowed, but an empty string meaning no number is valid.




### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()
# En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
# Vi kan skapa nästlade listor genom att öka indragnivån.
# Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
# Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
# Skapa en lista från en Microsoft Word-mall och anpassa de två första nivåerna i dess lista.
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
# Detta NumberFormat‑värde kommer att skapa stjärnformade punktlistsymboler.
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# Skapa stycken och applicera båda listnivåerna i vår anpassade listformatering på dem.
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

