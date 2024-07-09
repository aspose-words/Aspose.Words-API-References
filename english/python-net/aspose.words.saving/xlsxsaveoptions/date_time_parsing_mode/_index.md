---
title: XlsxSaveOptions.date_time_parsing_mode property
linktitle: date_time_parsing_mode property
articleTitle: date_time_parsing_mode property
second_title: Aspose.Words for Python
description: "XlsxSaveOptions.date_time_parsing_mode property. Gets or sets the mode that specifies how document text is parsed to identify date and time values"
type: docs
weight: 30
url: /python-net/aspose.words.saving/xlsxsaveoptions/date_time_parsing_mode/
---

## XlsxSaveOptions.date_time_parsing_mode property

Gets or sets the mode that specifies how document text is parsed to identify date and time values.
The default value is [XlsxDateTimeParsingMode.USE_CURRENT_LOCALE](../../xlsxdatetimeparsingmode/#USE_CURRENT_LOCALE).



```python
@property
def date_time_parsing_mode(self) -> aspose.words.saving.XlsxDateTimeParsingMode:
    ...

@date_time_parsing_mode.setter
def date_time_parsing_mode(self, value: aspose.words.saving.XlsxDateTimeParsingMode):
    ...

```

### Examples

Shows how to specify autodetection of the date time format.

```python
doc = aw.Document(file_name=MY_DIR + 'Xlsx DateTime.docx')
save_options = aw.saving.XlsxSaveOptions()
# Specify using datetime format autodetection.
save_options.date_time_parsing_mode = aw.saving.XlsxDateTimeParsingMode.AUTO
doc.save(file_name=ARTIFACTS_DIR + 'XlsxSaveOptions.DateTimeParsingMode.xlsx', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [XlsxSaveOptions](../)

