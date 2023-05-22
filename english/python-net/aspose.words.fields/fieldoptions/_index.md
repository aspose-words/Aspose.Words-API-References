﻿---
title: FieldOptions class
linktitle: FieldOptions class
articleTitle: FieldOptions class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldOptions class. Represents options to control field handling in a document"
type: docs
weight: 790
url: /python-net/aspose.words.fields/fieldoptions/
---

## FieldOptions class

Represents options to control field handling in a document.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [barcode_generator](./barcode_generator/) | Gets or set custom barcode generator. |
| [built_in_templates_paths](./built_in_templates_paths/) | Gets or sets paths of MS Word built-in templates. |
| [comparison_expression_evaluator](./comparison_expression_evaluator/) | Gets or sets the field comparison expressions evaluator. |
| [current_user](./current_user/) | Gets or sets the current user information. |
| [custom_toc_style_separator](./custom_toc_style_separator/) | Gets or sets custom style separator for the \\t switch in [FieldToc](../fieldtoc/) field. |
| [default_document_author](./default_document_author/) | Gets or sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered. |
| [field_database_provider](./field_database_provider/) | Gets or sets a provider that returns a query result for the [FieldDatabase](../fielddatabase/) field. |
| [field_index_format](./field_index_format/) | Gets or sets a [FieldOptions.field_index_format](./field_index_format/) that represents the formatting for the [FieldIndex](../fieldindex/) fields in the document. |
| [field_update_culture_provider](./field_update_culture_provider/) | Gets or sets a provider that returns a culture object specific for each particular field. |
| [field_update_culture_source](./field_update_culture_source/) | Specifies what culture to use to format the field result. |
| [field_updating_callback](./field_updating_callback/) | Gets or sets [IFieldUpdatingCallback](../ifieldupdatingcallback/) implementation |
| [field_updating_progress_callback](./field_updating_progress_callback/) | Gets or sets [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) implementation. |
| [file_name](./file_name/) | Gets or sets the file name of the document. |
| [is_bidi_text_supported_on_update](./is_bidi_text_supported_on_update/) | Gets or sets the value indicating whether bidirectional text is fully supported during field update or not. |
| [legacy_number_format](./legacy_number_format/) | Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [result_formatter](./result_formatter/) | Allows to control how the field result is formatted. |
| [template_name](./template_name/) | Gets or sets the file name of the template used by the document. |
| [toa_categories](./toa_categories/) | Gets or sets the table of authorities categories. |
| [use_invariant_culture_number_format](./use_invariant_culture_number_format/) | Gets or sets the value indicating that number format is parsed using invariant culture or not |
| [user_prompt_respondent](./user_prompt_respondent/) | Gets or sets the respondent to user prompts during field update. |

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

* module [aspose.words.fields](../)

