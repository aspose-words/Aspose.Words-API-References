---
title: FieldAddressBlock.language_id property
linktitle: language_id property
articleTitle: language_id property
second_title: Aspose.Words for Python
description: "FieldAddressBlock.language_id property. Gets or sets the language ID used to format the address."
type: docs
weight: 50
url: /tr/python-net/aspose.words.fields/fieldaddressblock/language_id/
---

## FieldAddressBlock.language_id property

Gets or sets the language ID used to format the address.


```python
@property
def language_id(self) -> str:
    ...

@language_id.setter
def language_id(self, value: str):
    ...

```

### Examples

Shows how to insert an ADDRESSBLOCK field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_ADDRESS_BLOCK, update_field=True).as_field_address_block()
self.assertEqual(' ADDRESSBLOCK ', field.get_field_code())
# Bunu "2" olarak ayarlamak, tüm ülkeleri ve bölgeleri dahil edecektir,
# ExcludedCountryOrRegionName özelliğinde belirtilen ülke veya bölge hariç.
field.include_country_or_region_name = '2'
field.format_address_on_country_or_region = True
field.excluded_country_or_region_name = 'United States'
field.name_and_address_format = '<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>'
# Varsayılan olarak, bu özellik belgenin ilk karakterinin dil kimliğini içerir.
# Alan için sonucu farklı bir kültürle biçimlendirmek üzere şöyle bir ayar yapabiliriz.
field.language_id = '1033'
self.assertEqual(' ADDRESSBLOCK  \\c 2 \\d \\e "United States" \\f "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>" \\l 1033', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAddressBlock](../)

