---
title: ListFormat.list_level_number property
linktitle: list_level_number property
articleTitle: list_level_number property
second_title: Aspose.Words for Python
description: "ListFormat.list_level_number property. Gets or sets the list level number (0 to 8) for the paragraph."
type: docs
weight: 40
url: /sv/python-net/aspose.words.lists/listformat/list_level_number/
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
# En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
# Vi kan skapa nästlade listor genom att öka indragnivån.
# Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
# Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
# Nedan är två typer av listor som vi kan skapa med en dokumentbyggare.
# 1 -  En punktlista:
# Denna lista kommer att applicera ett indrag och en punktmarkör ("•") före varje stycke.
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# Avsluta punktlistan.
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  En numrerad lista:
# Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje objekt.
builder.list_format.apply_number_default()
# Detta stycke är det första objektet. Det första objektet i en numrerad lista kommer att ha ett "1." som sin listpunktssymbol.
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# Anropa metoden "ListIndent" för att öka den aktuella listnivån,
# vilket kommer att starta en ny självständig lista med ett djupare indrag, vid det aktuella objektet på den första listnivån.
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# Det här är de första tre listobjekten på den andra listnivån, som kommer att behålla en räknare
# oberoende av räknaren på den första listnivån. Enligt det aktuella listformatet,
# kommer de att ha symbolerna "a.", "b." och "c.".
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# Anropa metoden "ListOutdent" för att återgå till föregående listnivå.
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# Dessa två stycken kommer att fortsätta räknaren på den första listnivån.
# Dessa objekt kommer att ha symbolerna "2." och "3."
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# Om vi öka listnivån till en nivå som vi tidigare har lagt till objekt på,
# kommer den nästlade listan att vara separat från den föregående, och dess numrering kommer att börja från början.
# Dessa listobjekt kommer att ha symbolerna "a.", "b.", "c.", "d.", och "e".
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# Minska indraget för listnivån igen.
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# Avsluta den numrerade listan.
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
# Vi kan skapa nästlade listor genom att öka indragnivån.
# Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
# Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
# Nedan är två typer av listor som vi kan skapa med en dokumentbyggare.
# 1 -  En numrerad lista:
# Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje objekt.
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# Genom att sätta egenskapen "ListLevelNumber" kan vi öka listnivån
# för att börja en självständig underlista vid det aktuella listobjektet.
# Microsoft Word-listmallen som heter "NumberDefault" använder siffror för att skapa listnivåer för den första listnivån.
# Djupare listnivåer använder bokstäver och gemena romerska siffror.
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  En punktlista:
# Denna lista kommer att applicera ett indrag och en punktmarkör ("•") före varje stycke.
# Djupare nivåer i denna lista kommer att använda olika symboler, såsom "■" och "○".
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# Vi kan inaktivera listformatering för att inte formatera efterföljande stycken som listor genom att avaktivera flaggan "List".
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)

