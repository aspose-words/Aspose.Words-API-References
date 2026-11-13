---
title: FieldAddressBlock.name_and_address_format property
linktitle: name_and_address_format property
articleTitle: name_and_address_format property
second_title: Aspose.Words for Python
description: "FieldAddressBlock.name_and_address_format property. Gets or sets the name and address format."
type: docs
weight: 60
url: /es/python-net/aspose.words.fields/fieldaddressblock/name_and_address_format/
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
# Establecer esto en "2" incluirá todos los países y regiones,
# a menos que sea el especificado en la propiedad ExcludedCountryOrRegionName.
field.include_country_or_region_name = '2'
field.format_address_on_country_or_region = True
field.excluded_country_or_region_name = 'United States'
field.name_and_address_format = '<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>'
# Por defecto, esta propiedad contendrá el ID de idioma del primer carácter del documento.
# Podemos establecer una cultura diferente para que el campo formatee el resultado de la siguiente manera.
field.language_id = '1033'
self.assertEqual(' ADDRESSBLOCK  \\c 2 \\d \\e "United States" \\f "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>" \\l 1033', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAddressBlock](../)

