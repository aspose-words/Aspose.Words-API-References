---
title: FieldListNum.starting_number property
linktitle: starting_number property
articleTitle: starting_number property
second_title: Aspose.Words for Python
description: "FieldListNum.starting_number property. Gets or sets the starting value for this field."
type: docs
weight: 50
url: /de/python-net/aspose.words.fields/fieldlistnum/starting_number/
---

## FieldListNum.starting_number property

Gets or sets the starting value for this field.


```python
@property
def starting_number(self) -> str:
    ...

@starting_number.setter
def starting_number(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# LISTNUM‑Felder zeigen eine Zahl an, die bei jedem LISTNUM‑Feld inkrementiert wird.
# Diese Felder verfügen außerdem über verschiedene Optionen, die es uns ermöglichen, sie zur Nachbildung nummerierter Listen zu verwenden.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Listen beginnen standardmäßig bei 1 zu zählen, aber wir können diese Zahl auf einen anderen Wert setzen, z. B. 0.
# Dieses Feld wird "0)" anzeigen.
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# LISTNUM‑Felder führen separate Zähler für jede Listenebene.
# Einfügen eines LISTNUM‑Feldes im selben Absatz wie ein anderes LISTNUM‑Feld
# erhöht die Listenebene statt des Zählers.
# Das nächste Feld wird die Zählung fortsetzen, die wir oben begonnen haben, und einen Wert von "1" auf Listenebene 1 anzeigen.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Dieses Feld startet eine Zählung auf Listenebene 2. Es wird einen Wert von "1" anzeigen.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Dieses Feld startet eine Zählung auf Listenebene 3. Es wird einen Wert von "1" anzeigen.
# Verschiedene Listenebenen haben unterschiedliche Formatierungen,
# so werden diese Felder kombiniert den Wert "1)a)i)" anzeigen.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# Das nächste LISTNUM‑Feld, das wir einfügen, wird die Zählung auf der Listenebene fortsetzen
# auf der das vorherige LISTNUM‑Feld war.
# Wir können die Eigenschaft "ListLevel" verwenden, um zu einer anderen Listenebene zu springen.
# Wenn dieses LISTNUM‑Feld auf Listenebene 3 bleiben würde, würde es "ii)" anzeigen,
# aber, da wir es auf Listenebene 2 verschoben haben, führt es die Zählung auf dieser Ebene fort und zeigt "b)" an.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# Wir können die Eigenschaft ListName festlegen, damit das Feld einen anderen AUTONUM‑Feldtyp emuliert.
# "NumberDefault" emuliert AUTONUM, "OutlineDefault" emuliert AUTONUMOUT,
# und "LegalDefault" emuliert AUTONUMLGL‑Felder.
# Der Listename "OutlineDefault" mit 1 als Startzahl führt dazu, dass "I." angezeigt wird.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# Der ListName wird nicht vom vorherigen Feld übernommen, daher müssen wir ihn für jedes neue Feld setzen.
# Dieses Feld setzt die Zählung mit dem anderen Listennamen fort und zeigt "II." an.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

