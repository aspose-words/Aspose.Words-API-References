---
title: SdtCalendarType Enum
linktitle: SdtCalendarType
articleTitle: SdtCalendarType
second_title: Aspose.Words for .NET
description: Explore Aspose.Words.Markup.SdtCalendarType enum to enhance your Office Open XML documents with versatile calendar options for better workflow efficiency.
type: docs
weight: 4550
url: /net/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enumeration

Specifies the possible types of calendars which can be used to specify [`CalendarType`](../structureddocumenttag/calendartype/) in an Office Open XML document.

```csharp
public enum SdtCalendarType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Default | `0` | Used as default value in OOXML. Equals Gregorian. |
| Gregorian | `0` | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. This calendar should be localized into the appropriate language. |
| GregorianArabic | `1` | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in Arabic. |
| GregorianMeFrench | `2` | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in Middle East French. |
| GregorianUs | `3` | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in English. |
| GregorianXlitEnglish | `4` | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be the representation of the English strings in the corresponding Arabic characters (the Arabic transliteration of the English for the Gregorian calendar). |
| GregorianXlitFrench | `5` | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be the representation of the French strings in the corresponding Arabic characters (the Arabic transliteration of the French for the Gregorian calendar). |
| Hebrew | `6` | Specifies that the Hebrew lunar calendar, as described by the Gauss formula for Passover [CITATION] and The Complete Restatement of Oral Law (Mishneh Torah),shall be used. |
| Hijri | `7` | Specifies that the Hijri lunar calendar, as described by the Kingdom of Saudi Arabia, Ministry of Islamic Affairs, Endowments, Da‘wah and Guidance, shall be used. |
| Japan | `8` | Specifies that the Japanese Emperor Era calendar, as described by Japanese Industrial Standard JIS X 0301, shall be used. |
| Korea | `9` | Specifies that the Korean Tangun Era calendar, as described by Korean Law Enactment No. 4, shall be used. |
| None | `10` | Specifies that no calendar should be used. |
| Saka | `11` | Specifies that the Saka Era calendar, as described by the Calendar Reform Committee of India, as part of the Indian Ephemeris and Nautical Almanac, shall be used. |
| Taiwan | `12` | Specifies that the Taiwanese calendar, as defined by the Chinese National Standard CNS 7648, shall be used. |
| Thai | `13` | Specifies that the Thai calendar, as defined by the Royal Decree of H.M. King Vajiravudh (Rama VI) in Royal Gazette B. E. 2456 (1913 A.D.) and by the decree of Prime Minister Phibunsongkhram (1941 A.D.) to start the year on the Gregorian January 1 and to map year zero to Gregorian year 543 B.C., shall be used. |

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
