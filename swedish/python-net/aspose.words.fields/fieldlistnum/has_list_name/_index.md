---
title: FieldListNum.has_list_name property
linktitle: has_list_name property
articleTitle: has_list_name property
second_title: Aspose.Words for Python
description: "FieldListNum.has_list_name property. Returns a value indicating whether the name of an abstract numbering definition is provided by the field's code."
type: docs
weight: 20
url: /sv/python-net/aspose.words.fields/fieldlistnum/has_list_name/
---

## FieldListNum.has_list_name property

Returns a value indicating whether the name of an abstract numbering definition
is provided by the field's code.


```python
@property
def has_list_name(self) -> bool:
    ...

```

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# LISTNUM-fält visar ett tal som ökar vid varje LISTNUM-fält.
# Dessa fält har också en mängd alternativ som låter oss använda dem för att efterlikna numrerade listor.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Listor börjar räkna från 1 som standard, men vi kan sätta detta tal till ett annat värde, till exempel 0.
# Detta fält kommer att visa "0)".
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# LISTNUM-fält behåller separata räknare för varje listnivå.
# Att infoga ett LISTNUM-fält i samma stycke som ett annat LISTNUM-fält
# ökar listnivån istället för räknaren.
# Det nästa fältet kommer att fortsätta räknaren som vi startade ovan och visa värdet "1" på listnivå 1.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Detta fält kommer att starta en räknare på listnivå 2. Det kommer att visa värdet "1".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Detta fält kommer att starta en räknare på listnivå 3. Det kommer att visa värdet "1".
# Olika listnivåer har olika formatering,
# så dessa fält kombinerade kommer att visa ett värde av "1)a)i)".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# Nästa LISTNUM-fält som vi infogar kommer att fortsätta räkningen på listnivån
# som det föregående LISTNUM-fältet var på.
# Vi kan använda egenskapen "ListLevel" för att hoppa till en annan listnivå.
# Om detta LISTNUM-fält stannade på listnivå 3, skulle det visa "ii)",
# men, eftersom vi har flyttat det till listnivå 2, fortsätter det räkningen på den nivån och visar "b)".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# Vi kan sätta egenskapen ListName för att få fältet att efterlikna en annan AUTONUM-fälttyp.
# "NumberDefault" efterliknar AUTONUM, "OutlineDefault" efterliknar AUTONUMOUT,
# och "LegalDefault" efterliknar AUTONUMLGL-fält.
# Listnamnet "OutlineDefault" med 1 som startnummer kommer att resultera i att visa "I.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# ListName överförs inte från föregående fält, så vi måste sätta den för varje nytt fält.
# Detta fält fortsätter räkningen med det olika listnamnet och visar "II.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

