---
title: ListFormat.apply_bullet_default method
linktitle: apply_bullet_default method
articleTitle: apply_bullet_default method
second_title: Aspose.Words for Python
description: "ListFormat.apply_bullet_default method. Starts a new default bulleted list and applies it to the paragraph."
type: docs
weight: 50
url: /sv/python-net/aspose.words.lists/listformat/apply_bullet_default/
---

## apply_bullet_default() {#default}

Starts a new default bulleted list and applies it to the paragraph.


```python
def apply_bullet_default(self):
    ...
```

### Remarks

This is a shortcut method that creates a new list using the default bulleted
template, applies it to the paragraph and selects the 1st list level.




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

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)
* method [ListFormat.remove_numbers()](../remove_numbers/#default)
* property [ListFormat.list_level_number](../list_level_number/)

