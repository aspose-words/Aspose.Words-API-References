---
title: FieldAddressBlock.excluded_country_or_region_name property
linktitle: excluded_country_or_region_name property
articleTitle: excluded_country_or_region_name property
second_title: Aspose.Words for Python
description: "FieldAddressBlock.excluded_country_or_region_name property. Gets or sets the excluded country/region name."
type: docs
weight: 20
url: /python-net/aspose.words.fields/fieldaddressblock/excluded_country_or_region_name/
---

## FieldAddressBlock.excluded_country_or_region_name property

Gets or sets the excluded country/region name.


### Examples

Shows how to insert an ADDRESSBLOCK field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

field = builder.insert_field(aw.fields.FieldType.FIELD_ADDRESS_BLOCK, True).as_field_address_block()

self.assertEqual(" ADDRESSBLOCK ", field.get_field_code())

# Setting this to "2" will include all countries and regions,
# unless it is the one specified in the "excluded_country_or_region_name" property.
field.include_country_or_region_name = "2"
field.format_address_on_country_or_region = True
field.excluded_country_or_region_name = "United States"
field.name_and_address_format = "<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>"

# By default, this property will contain the language ID of the first character of the document.
# We can set a different culture for the field to format the result with like this.
field.language_id = "1033" # en-US

self.assertEqual(
    " ADDRESSBLOCK  \\c 2 \\d \\e \"United States\" \\f \"<Title> <Forename> <Surname> <Address Line 1> <Region> <Postcode> <Country>\" \\l 1033",
    field.get_field_code())
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAddressBlock](../)

