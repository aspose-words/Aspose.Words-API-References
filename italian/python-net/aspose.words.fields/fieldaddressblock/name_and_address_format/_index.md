---
title: FieldAddressBlock.name_and_address_format property
linktitle: name_and_address_format property
articleTitle: name_and_address_format property
second_title: Aspose.Words for Python
description: "FieldAddressBlock.name_and_address_format property. Gets or sets the name and address format."
type: docs
weight: 60
url: /it/python-net/aspose.words.fields/fieldaddressblock/name_and_address_format/
---

## FieldAddressBlock.name_and_address_format property

Gets or sets the name and address format.


```python
@property
def name_and_address_format(self) -> str:
    ...

@name_and_address_format.setter
def name_and_address_format(self, value: str):
    ...

```

### Examples

Shows how to insert an ADDRESSBLOCK field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_ADDRESS_BLOCK, update_field=True).as_field_address_block()
self.assertEqual(' ADDRESSBLOCK ', field.get_field_code())
# Impostare questo su \"2\" includerà tutti i paesi e le regioni,
# a meno che non sia quello specificato nella proprietà ExcludedCountryOrRegionName.
field.include_country_or_region_name = '2'
field.format_address_on_country_or_region = True
field.excluded_country_or_region_name = 'United States'
field.name_and_address_format = '<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>'
# Per impostazione predefinita, questa proprietà conterrà l'ID lingua del primo carattere del documento.
# Possiamo impostare una cultura diversa per il campo per formattare il risultato in questo modo.
field.language_id = '1033'
self.assertEqual(' ADDRESSBLOCK  \\c 2 \\d \\e "United States" \\f "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>" \\l 1033', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAddressBlock](../)

