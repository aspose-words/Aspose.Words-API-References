---
title: SdtDateStorageFormat Enum
linktitle: SdtDateStorageFormat
articleTitle: SdtDateStorageFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Markup.SdtDateStorageFormat enum. Specifies how the date for a date SDT is stored/retrieved when the SDT is bound to an XML node in the documents data store in C#.
type: docs
weight: 4330
url: /net/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enumeration

Specifies how the date for a date SDT is stored/retrieved when the SDT is bound to an XML node in the document's data store.

```csharp
public enum SdtDateStorageFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Date | `0` | The date value for a date SDT is stored as a date in the standard XML Schema Date format. |
| DateTime | `1` | The date value for a date SDT is stored as a date in the standard XML Schema DateTime format. |
| Text | `2` | The date value for a date SDT is stored as text. |
| Default | `1` | Defaults to DateTime |

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

* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
