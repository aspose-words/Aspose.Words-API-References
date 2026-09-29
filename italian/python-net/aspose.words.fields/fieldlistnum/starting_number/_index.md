---
title: FieldListNum.starting_number property
linktitle: starting_number property
articleTitle: starting_number property
second_title: Aspose.Words for Python
description: "FieldListNum.starting_number property. Gets or sets the starting value for this field."
type: docs
weight: 50
url: /it/python-net/aspose.words.fields/fieldlistnum/starting_number/
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
# I campi LISTNUM visualizzano un numero che si incrementa ad ogni campo LISTNUM.
# Questi campi hanno anche una varietà di opzioni che ci permettono di usarli per emulare elenchi numerati.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Gli elenchi iniziano a contare da 1 per impostazione predefinita, ma possiamo impostare questo numero a un valore diverso, ad esempio 0.
# Questo campo visualizzerà "0)".
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# I campi LISTNUM mantengono conteggi separati per ogni livello di elenco.
# Inserire un campo LISTNUM nello stesso paragrafo di un altro campo LISTNUM
# aumenta il livello dell'elenco invece del conteggio.
# Il campo successivo continuerà il conteggio che abbiamo iniziato sopra e visualizzerà un valore di "1" al livello di elenco 1.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Questo campo avvierà un conteggio al livello di elenco 2. Visualizzerà un valore di "1".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Questo campo avvierà un conteggio al livello di elenco 3. Visualizzerà un valore di "1".
# I diversi livelli di elenco hanno formattazioni diverse,
# quindi questi campi combinati visualizzeranno un valore di "1)a)i)".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# Il prossimo campo LISTNUM che inseriamo continuerà il conteggio al livello di elenco
# su cui era il campo LISTNUM precedente.
# Possiamo usare la proprietà "ListLevel" per passare a un diverso livello di elenco.
# Se questo campo LISTNUM rimaneva al livello di elenco 3, visualizzerebbe "ii)",
# ma, poiché lo abbiamo spostato al livello di elenco 2, continua il conteggio a quel livello e visualizza "b)".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# Possiamo impostare la proprietà ListName per far sì che il campo emuli un diverso tipo di campo AUTONUM.
# "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
# e "LegalDefault" emula i campi AUTONUMLGL.
# Il nome di elenco "OutlineDefault" con 1 come numero iniziale produrrà la visualizzazione di "I.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# Il ListName non viene mantenuto dal campo precedente, quindi dovremo impostarlo per ogni nuovo campo.
# Questo campo continua il conteggio con il nome di elenco diverso e visualizza "II.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

