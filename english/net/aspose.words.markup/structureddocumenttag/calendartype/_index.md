---
title: StructuredDocumentTag.CalendarType
linktitle: CalendarType
articleTitle: CalendarType
second_title: Aspose.Words for .NET
description: Discover the StructuredDocumentTag CalendarType property to customize your SDT calendar type. Enhance your documents with tailored calendar options!
type: docs
weight: 50
url: /net/aspose.words.markup/structureddocumenttag/calendartype/
---
## StructuredDocumentTag.CalendarType property

Specifies the type of calendar for this **SDT**. Default is Default

```csharp
public SdtCalendarType CalendarType { get; set; }
```

## Remarks

Accessing this property will only work for Date SDT type.

For all other SDT types exception will occur.

## Examples

Shows how to prompt the user to enter a date with a structured document tag.

```csharp
Document doc = new Document();

// Insert a structured document tag that prompts the user to enter a date.
// In Microsoft Word, this element is known as a "Date picker content control".
// When we click on the arrow on the right end of this tag in Microsoft Word,
// we will see a pop up in the form of a clickable calendar.
// We can use that popup to select a date that the tag will display.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Display the date, according to the Saudi Arabian Arabic locale.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Set the format with which to display the date.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Display the date according to the Hijri calendar.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
// According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### See Also

* enum [SdtCalendarType](../../sdtcalendartype/)
* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
