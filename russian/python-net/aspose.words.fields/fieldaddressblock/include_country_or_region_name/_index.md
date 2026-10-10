---
title: FieldAddressBlock.include_country_or_region_name property
linktitle: include_country_or_region_name property
articleTitle: include_country_or_region_name property
second_title: Aspose.Words for Python
description: "FieldAddressBlock.include_country_or_region_name property. Gets or sets whether to include the name of the country/region."
type: docs
weight: 40
url: /ru/python-net/aspose.words.fields/fieldaddressblock/include_country_or_region_name/
---

## FieldAddressBlock.include_country_or_region_name property

Gets or sets whether to include the name of the country/region.


```python
@property
def include_country_or_region_name(self) -> str:
    ...

@include_country_or_region_name.setter
def include_country_or_region_name(self, value: str):
    ...

```

### Examples

Shows how to insert an ADDRESSBLOCK field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_ADDRESS_BLOCK, update_field=True).as_field_address_block()
self.assertEqual(' ADDRESSBLOCK ', field.get_field_code())
# Установка этого значения в "2" включит все страны и регионы,
# если только это не тот, который указан в свойстве ExcludedCountryOrRegionName.
field.include_country_or_region_name = '2'
field.format_address_on_country_or_region = True
field.excluded_country_or_region_name = 'United States'
field.name_and_address_format = '<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>'
# По умолчанию это свойство будет содержать идентификатор языка первого символа документа.
# Мы можем установить другую культуру для поля, чтобы отформатировать результат, например, так.
field.language_id = '1033'
self.assertEqual(' ADDRESSBLOCK  \\c 2 \\d \\e "United States" \\f "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>" \\l 1033', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAddressBlock](../)

