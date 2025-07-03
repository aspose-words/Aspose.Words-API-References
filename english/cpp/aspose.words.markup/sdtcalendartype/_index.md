---
title: Aspose::Words::Markup::SdtCalendarType enum
linktitle: SdtCalendarType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::SdtCalendarType enum. Specifies the possible types of calendars which can be used to specify CalendarType in an Office Open XML document in C++.'
type: docs
weight: 19000
url: /cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


Specifies the possible types of calendars which can be used to specify [CalendarType](../structureddocumenttag/get_calendartype/) in an Office Open XML document.

```cpp
enum class SdtCalendarType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Default | 0 | Used as default value in OOXML. Equals [Gregorian](./). |
| Gregorian | n/a | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. This calendar should be localized into the appropriate language. |
| GregorianArabic | n/a | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in Arabic. |
| GregorianMeFrench | n/a | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in Middle East French. |
| GregorianUs | n/a | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in English. |
| GregorianXlitEnglish | n/a | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be the representation of the English strings in the corresponding Arabic characters (the Arabic transliteration of the English for the Gregorian calendar). |
| GregorianXlitFrench | n/a | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be the representation of the French strings in the corresponding Arabic characters (the Arabic transliteration of the French for the Gregorian calendar). |
| Hebrew | n/a | Specifies that the Hebrew lunar calendar, as described by the Gauss formula for Passover [CITATION] and The Complete Restatement of Oral Law (Mishneh Torah),shall be used. |
| Hijri | n/a | Specifies that the Hijri lunar calendar, as described by the Kingdom of Saudi Arabia, Ministry of Islamic Affairs, Endowments, Da‘wah and Guidance, shall be used. |
| Japan | n/a | Specifies that the Japanese Emperor Era calendar, as described by Japanese Industrial Standard JIS X 0301, shall be used. |
| Korea | n/a | Specifies that the Korean Tangun Era calendar, as described by Korean Law Enactment No. 4, shall be used. |
| None | n/a | Specifies that no calendar should be used. |
| Saka | n/a | Specifies that the Saka Era calendar, as described by the Calendar Reform Committee of India, as part of the Indian Ephemeris and Nautical Almanac, shall be used. |
| Taiwan | n/a | Specifies that the Taiwanese calendar, as defined by the Chinese National Standard CNS 7648, shall be used. |
| Thai | n/a | Specifies that the Thai calendar, as defined by the Royal Decree of H.M. King Vajiravudh (Rama VI) in Royal Gazette B. E. 2456 (1913 A.D.) and by the decree of Prime Minister Phibunsongkhram (1941 A.D.) to start the year on the Gregorian January 1 and to map year zero to Gregorian year 543 B.C., shall be used. |


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
