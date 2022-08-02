---
title: locale_id property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the LCID of the field."
type: docs
weight: 60
url: /python-net/aspose.words.fields/field/locale_id/
---

## Field.locale_id property

Gets or sets the LCID of the field.


### Examples

Shows how to insert a field and work with its locale.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a DATE field, and then print the date it will display.
# Your thread's current culture determines the formatting of the date.
field = builder.insert_field("DATE")
print(f"Today's date, as displayed in the \"{CultureInfo.current_culture.english_name}\" culture: {field.result}")

self.assertEqual(1033, field.locale_id)

# Changing the culture of our thread will impact the result of the DATE field.
# Another way to get the DATE field to display a date in a different culture is to use its LocaleId property.
# This way allows us to avoid changing the thread's culture to get this effect.
doc.field_options.field_update_culture_source = aw.fields.FieldUpdateCultureSource.FIELD_CODE
de_culture = CultureInfo("de-DE")
field.locale_id = de_culture.LCID
field.update()

print(f"Today's date, as displayed according to the \"{CultureInfo.get_culture_info(field.LocaleId).english_name}\" culture: {field.Result}")
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)
* enum value [FieldUpdateCultureSource.FIELD_CODE](../../fieldupdateculturesource/#FIELD_CODE)

