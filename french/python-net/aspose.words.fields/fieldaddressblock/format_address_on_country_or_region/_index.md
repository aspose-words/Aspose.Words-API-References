---
title: FieldAddressBlock.format_address_on_country_or_region property
linktitle: format_address_on_country_or_region property
articleTitle: format_address_on_country_or_region property
second_title: Aspose.Words for Python
description: "FieldAddressBlock.format_address_on_country_or_region property. Gets or sets whether to format the address according to the country/region of the recipient as defined by POST*CODE (Universal Postal Union 2006)."
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldaddressblock/format_address_on_country_or_region/
---

## FieldAddressBlock.format_address_on_country_or_region property

Gets or sets whether to format the address according to the country/region of the recipient
as defined by POST\*CODE (Universal Postal Union 2006).


```python
@property
def format_address_on_country_or_region(self) -> bool:
    ...

@format_address_on_country_or_region.setter
def format_address_on_country_or_region(self, value: bool):
    ...

```

### Examples

Shows how to insert an ADDRESSBLOCK field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_ADDRESS_BLOCK, update_field=True).as_field_address_block()
self.assertEqual(' ADDRESSBLOCK ', field.get_field_code())
# Définir ceci à \"2\" inclura tous les pays et régions,
# sauf celui spécifié dans la propriété ExcludedCountryOrRegionName.
field.include_country_or_region_name = '2'
field.format_address_on_country_or_region = True
field.excluded_country_or_region_name = 'United States'
field.name_and_address_format = '<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>'
# Par défaut, cette propriété contiendra l'ID de langue du premier caractère du document.
# Nous pouvons définir une culture différente pour le champ afin de formater le résultat ainsi.
field.language_id = '1033'
self.assertEqual(' ADDRESSBLOCK  \\c 2 \\d \\e "United States" \\f "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>" \\l 1033', field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAddressBlock](../)

