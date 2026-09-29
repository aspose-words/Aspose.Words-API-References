---
title: ListLevel.number_position property
linktitle: number_position property
articleTitle: number_position property
second_title: Aspose.Words for Python
description: "ListLevel.number_position property. Returns or sets the position (in points) of the number or bullet for the list level."
type: docs
weight: 80
url: /sv/python-net/aspose.words.lists/listlevel/number_position/
---

## ListLevel.number_position property

Returns or sets the position (in points) of the number or bullet for the list level.


```python
@property
def number_position(self) -> float:
    ...

@number_position.setter
def number_position(self, value: float):
    ...

```

### Remarks

[ListLevel.number_position](./) corresponds to LeftIndent plus FirstLineIndent of the paragraph.




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

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)
* property [ListLevel.text_position](../text_position/)
* property [ListLevel.tab_position](../tab_position/)

