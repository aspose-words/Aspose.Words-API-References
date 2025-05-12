---
title: XlsxDateTimeParsingMode enumeration
linktitle: XlsxDateTimeParsingMode enumeration
articleTitle: XlsxDateTimeParsingMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.XlsxDateTimeParsingMode enumeration. Specifies how document text is parsed to identify date and time values."
type: docs
weight: 920
url: /python-net/aspose.words.saving/xlsxdatetimeparsingmode/
---

## XlsxDateTimeParsingMode enumeration

Specifies how document text is parsed to identify date and time values.


### Members

| Name | Description |
| --- | --- |
| USE_CURRENT_LOCALE | The datetime format set for the current thread is used first to parse string values. If the parsing fails, other common datetime formats are tried. |
| AUTO | The datetime format used in a document is determined automatically. This may take additional time. |

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

* module [aspose.words.saving](../)

