---
title: FieldOptions.field_update_culture_source property
linktitle: field_update_culture_source property
articleTitle: field_update_culture_source property
second_title: Aspose.Words for Python
description: "FieldOptions.field_update_culture_source property. Specifies what culture to use to format the field result."
type: docs
weight: 100
url: /python-net/aspose.words.fields/fieldoptions/field_update_culture_source/
---

## FieldOptions.field_update_culture_source property

Specifies what culture to use to format the field result.

By default, the culture of the current thread is used.

The setting affects only date/time fields with \\\\@ format switch.




### Examples

Shows how to specify the source of the culture used for date formatting during a field update or mail merge.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert two merge fields with German locale.
builder.font.locale_id = CultureInfo("de-DE").lcid
builder.insert_field("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"")
builder.write(" - ")
builder.insert_field("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"")

# Set the current culture to US English after preserving its original value in a variable.
current_culture = Thread.current_thread.current_culture
Thread.current_thread.current_culture = CultureInfo("en-US")

# This merge will use the current thread's culture to format the date, US English.
doc.mail_merge.execute(["Date1"], [datetime(2020, 1, 1)])

# Configure the next merge to source its culture value from the field code. The value of that culture will be German.
doc.field_options.field_update_culture_source = aw.fields.FieldUpdateCultureSource.FIELD_CODE
doc.mail_merge.execute(["Date2"], [datetime(2020, 1, 1)])

# The first merge result contains a date formatted in English, while the second one is in German.
self.assertEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.range.text.strip())

# Restore the thread's original culture.
Thread.current_thread.current_culture = current_culture
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

