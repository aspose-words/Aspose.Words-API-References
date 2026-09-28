---
title: FieldAddressBlock.name_and_address_format property
linktitle: name_and_address_format property
articleTitle: name_and_address_format property
second_title: Aspose.Words for Python
description: "FieldAddressBlock.name_and_address_format property. Gets or sets the name and address format."
type: docs
weight: 60
url: /ar/python-net/aspose.words.fields/fieldaddressblock/name_and_address_format/
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
# ضبط هذا على "2" سيشمل جميع البلدان والمناطق،
# إلا إذا كان هو المحدد في خاصية ExcludedCountryOrRegionName.
field.include_country_or_region_name = '2'
field.format_address_on_country_or_region = True
field.excluded_country_or_region_name = 'United States'
field.name_and_address_format = '<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>'
# بشكل افتراضي، ستحتوي هذه الخاصية على معرف اللغة للحرف الأول في المستند.
# يمكننا تعيين ثقافة مختلفة للحقل لتنسيق النتيجة بهذه الطريقة.
field.language_id = '1033'
self.assertEqual(' ADDRESSBLOCK  \\c 2 \\d \\e "United States" \\f "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>" \\l 1033', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAddressBlock](../)

