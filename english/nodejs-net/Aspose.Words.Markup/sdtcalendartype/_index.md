---
title: SdtCalendarType enumeration
linktitle: SdtCalendarType enumeration
articleTitle: SdtCalendarType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Markup.SdtCalendarType enumeration. Specifies the possible types of calendars which can be used to specify [StructuredDocumentTag.calendarType](../structureddocumenttag/calendarType/) in an Office Open XML document."
type: docs
weight: 110
url: /nodejs-net/aspose.words.markup/sdtcalendartype/
---

## SdtCalendarType enumeration

Specifies the possible types of calendars which can be used to specify [StructuredDocumentTag.calendarType](../structureddocumenttag/calendarType/)
in an Office Open XML document.



### Members

| Name | Description |
| --- | --- |
| Default | Used as default value in OOXML. Equals [SdtCalendarType.Gregorian](./#Gregorian). |
| Gregorian | Specifies that the Gregorian calendar, as defined in ISO  8601, shall be used.  This calendar should be localized into the appropriate language. |
| GregorianArabic | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in Arabic. |
| GregorianMeFrench | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in Middle East French. |
| GregorianUs | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in English. |
| GregorianXlitEnglish | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be the representation of the English strings in the corresponding Arabic characters  (the Arabic transliteration of the English for the Gregorian calendar). |
| GregorianXlitFrench | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be the representation of the French strings in the corresponding Arabic characters  (the Arabic transliteration of the French for the Gregorian calendar). |
| Hebrew | Specifies that the Hebrew lunar calendar, as described by the Gauss formula for Passover [CITATION]  and The Complete Restatement of Oral Law (Mishneh Torah),shall be used. |
| Hijri | Specifies that the Hijri lunar calendar, as described by the Kingdom of Saudi Arabia,  Ministry of Islamic Affairs, Endowments, Da‘wah and Guidance, shall be used. |
| Japan | Specifies that the Japanese Emperor Era calendar, as described by  Japanese Industrial Standard JIS X 0301, shall be used. |
| Korea | Specifies that the Korean Tangun Era calendar,  as described by Korean Law Enactment No. 4, shall be used. |
| None | Specifies that no calendar should be used. |
| Saka | Specifies that the Saka Era calendar, as described by the Calendar Reform Committee of India,  as part of the Indian Ephemeris and Nautical Almanac, shall be used. |
| Taiwan | Specifies that the Taiwanese calendar, as defined by the Chinese National Standard CNS 7648, shall be used. |
| Thai | Specifies that the Thai calendar, as defined by the Royal Decree of H.M. King Vajiravudh (Rama VI) in  Royal Gazette B. E. 2456 (1913 A.D.) and by the decree of Prime Minister Phibunsongkhram (1941 A.D.) to  start the year on the Gregorian January 1 and to map year zero to Gregorian year 543 B.C., shall be used. |

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

* module [Aspose.Words.Markup](../)

