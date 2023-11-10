---
title: StructuredDocumentTag.calendar_type property
linktitle: calendar_type property
articleTitle: calendar_type property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.calendar_type property. Specifies the type of calendar for this SDT"
type: docs
weight: 50
url: /python-net/aspose.words.markup/structureddocumenttag/calendar_type/
---

## StructuredDocumentTag.calendar_type property

Specifies the type of calendar for this **SDT**.
Default is [SdtCalendarType.DEFAULT](../../sdtcalendartype/#DEFAULT)



```python
@property
def calendar_type(self) -> aspose.words.markup.SdtCalendarType:
    ...

@calendar_type.setter
def calendar_type(self, value: aspose.words.markup.SdtCalendarType):
    ...

```

### Remarks

Accessing this property will only work for [SdtType.DATE](../../sdttype/#DATE) SDT type.


For all other SDT types exception will occur.




### Examples

Shows how to prompt the user to enter a date with a structured document tag.

```python
doc = aw.Document()

# Insert a structured document tag that prompts the user to enter a date.
# In Microsoft Word, this element is known as a "Date picker content control".
# When we click on the arrow on the right end of this tag in Microsoft Word,
# we will see a pop up in the form of a clickable calendar.
# We can use that popup to select a date that the tag will display.
sdt_date = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.DATE, aw.markup.MarkupLevel.INLINE)

# Display the date, according to the Saudi Arabian Arabic locale.
sdt_date.date_display_locale = 1025 #CultureInfo.get_culture_info("ar-SA").LCID

# Set the format with which to display the date.
sdt_date.date_display_format = "dd MMMM, yyyy"
sdt_date.date_storage_format = aw.markup.SdtDateStorageFormat.DATE_TIME

# Display the date according to the Hijri calendar.
sdt_date.calendar_type = aw.markup.SdtCalendarType.HIJRI

# Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
# According to the tag's calendar, set the "full_date" property to get the tag to display a default date.
sdt_date.full_date = datetime(1440, 10, 20)

builder = aw.DocumentBuilder(doc)
builder.insert_node(sdt_date)

doc.save(ARTIFACTS_DIR + "StructuredDocumentTag.date.docx")
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

