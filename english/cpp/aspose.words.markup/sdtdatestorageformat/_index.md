---
title: Aspose::Words::Markup::SdtDateStorageFormat enum
linktitle: SdtDateStorageFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::SdtDateStorageFormat enum. Specifies how the date for a date SDT is stored/retrieved when the SDT is bound to an XML node in the document''s data store in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enum


Specifies how the date for a date SDT is stored/retrieved when the SDT is bound to an XML node in the document's data store.

```cpp
enum class SdtDateStorageFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Date | 0 | The date value for a date SDT is stored as a date in the standard XML Schema Date format. |
| DateTime | 1 | The date value for a date SDT is stored as a date in the standard XML Schema DateTime format. |
| Text | 2 | The date value for a date SDT is stored as text. |
| Default | n/a | Defaults to [DateTime](./) |


## Examples



Shows how to prompt the user to enter a date with a structured document tag. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Insert a structured document tag that prompts the user to enter a date.
// In Microsoft Word, this element is known as a "Date picker content control".
// When we click on the arrow on the right end of this tag in Microsoft Word,
// we will see a pop up in the form of a clickable calendar.
// We can use that popup to select a date that the tag will display.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Display the date, according to the Saudi Arabian Arabic locale.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Set the format with which to display the date.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Display the date according to the Hijri calendar.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
// According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## See Also

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
