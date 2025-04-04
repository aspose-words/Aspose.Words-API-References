---
title: StructuredDocumentTag.calendarType property
linktitle: calendarType property
articleTitle: calendarType property
second_title: Aspose.Words for Node.js
description: "StructuredDocumentTag.calendarType property. Specifies the type of calendar for this SDT"
type: docs
weight: 50
url: /nodejs-net/aspose.words.markup/structureddocumenttag/calendarType/
---

## StructuredDocumentTag.calendarType property

Specifies the type of calendar for this **SDT**.
Default is [SdtCalendarType.Default](../../sdtcalendartype/#Default)



```js
get calendarType(): Aspose.Words.Markup.SdtCalendarType
```

### Remarks

Accessing this property will only work for [SdtType.Date](../../sdttype/#Date) SDT type.


For all other SDT types exception will occur.




### Examples

Shows how to prompt the user to enter a date with a structured document tag.

```js
let doc = new aw.Document();

// Insert a structured document tag that prompts the user to enter a date.
// In Microsoft Word, this element is known as a "Date picker content control".
// When we click on the arrow on the right end of this tag in Microsoft Word,
// we will see a pop up in the form of a clickable calendar.
// We can use that popup to select a date that the tag will display.
let sdtDate = new aw.Markup.StructuredDocumentTag(doc, aw.Markup.SdtType.Date, aw.Markup.MarkupLevel.Inline);

// Display the date, according to the Saudi Arabian Arabic locale.
sdtDate.dateDisplayLocale = 1025;//CultureInfo.GetCultureInfo("ar-SA").LCID;

// Set the format with which to display the date.
sdtDate.dateDisplayFormat = "dd MMMM, yyyy";
sdtDate.dateStorageFormat = aw.Markup.SdtDateStorageFormat.DateTime;

// Display the date according to the Hijri calendar.
sdtDate.calendarType = aw.Markup.SdtCalendarType.Hijri;

// Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
// According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
sdtDate.fullDate = new Date(1440, 9, 20);

let builder = new aw.DocumentBuilder(doc);
builder.insertNode(sdtDate);

doc.save(base.artifactsDir + "StructuredDocumentTag.date.docx");
```

### See Also

* module [Aspose.Words.Markup](../../)
* class [StructuredDocumentTag](../)

