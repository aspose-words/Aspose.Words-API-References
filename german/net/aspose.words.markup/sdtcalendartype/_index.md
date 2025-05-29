---
title: SdtCalendarType Enum
linktitle: SdtCalendarType
articleTitle: SdtCalendarType
second_title: Aspose.Words für .NET
description: Erkunden Sie die Aufzählung Aspose.Words.Markup.SdtCalendarType, um Ihre Office Open XML-Dokumente mit vielseitigen Kalenderoptionen für eine bessere Arbeitsablaufeffizienz zu verbessern.
type: docs
weight: 4690
url: /de/net/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enumeration

Gibt die möglichen Kalendertypen an, die verwendet werden können, um[`CalendarType`](../structureddocumenttag/calendartype/) in einem Office Open XML-Dokument.

```csharp
public enum SdtCalendarType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Default | `0` | Wird als Standardwert in OOXML verwendet. GleichGregorian . |
| Gregorian | `0` | Gibt an, dass der Gregorianische Kalender gemäß ISO 8601 verwendet werden soll. Dieser Kalender sollte in die entsprechende Sprache übersetzt werden. |
| GregorianArabic | `1` | Gibt an, dass der Gregorianische Kalender gemäß ISO 8601 verwendet werden soll. Die Werte für diesen Kalender sollten auf Arabisch angegeben werden. |
| GregorianMeFrench | `2` | Gibt an, dass der Gregorianische Kalender gemäß ISO 8601 verwendet werden soll. Die Werte für diesen Kalender sollten in nahöstlichem Französisch angegeben werden. |
| GregorianUs | `3` | Gibt an, dass der Gregorianische Kalender gemäß ISO 8601 verwendet werden soll. Die Werte für diesen Kalender sollten in Englisch angegeben werden. |
| GregorianXlitEnglish | `4` | Gibt an, dass der Gregorianische Kalender gemäß ISO 8601 verwendet werden soll. Die Werte für diesen Kalender sollten die Darstellung der englischen Zeichenfolgen in den entsprechenden arabischen Zeichen sein (die arabische Transliteration des Englischen für den Gregorianischen Kalender). |
| GregorianXlitFrench | `5` | Gibt an, dass der Gregorianische Kalender gemäß ISO 8601 verwendet werden soll. Die Werte für diesen Kalender sollten die Darstellung der französischen Zeichenfolgen in den entsprechenden arabischen Zeichen sein (die arabische Transliteration des Französischen für den Gregorianischen Kalender). |
| Hebrew | `6` | Gibt an, dass der hebräische Mondkalender, wie er in der Gauß-Formel für Pessach [ZITAT] und der vollständigen Neufassung des mündlichen Gesetzes (Mischne Tora) beschrieben wird, verwendet werden soll. |
| Hijri | `7` | Gibt an, dass der Hijri-Mondkalender, wie vom Königreich Saudi-Arabien, Ministerium für islamische Angelegenheiten, Stiftungen, Da'wah und Führung beschrieben, verwendet werden soll. |
| Japan | `8` | Gibt an, dass der Kalender der japanischen Kaiserzeit, wie im japanischen Industriestandard JIS X 0301 beschrieben, verwendet werden soll. |
| Korea | `9` | Gibt an, dass der koreanische Tangun-Kalender, wie im koreanischen Gesetz Nr. 4 beschrieben, verwendet werden soll. |
| None | `10` | Gibt an, dass kein Kalender verwendet werden soll. |
| Saka | `11` | Gibt an, dass der Saka-Ära-Kalender, wie vom Calendar Reform Committee of India beschrieben, als Teil der Indian Ephemeris and Nautical Almanac, verwendet werden soll. |
| Taiwan | `12` | Gibt an, dass der taiwanesische Kalender gemäß der chinesischen nationalen Norm CNS 7648 verwendet werden soll. |
| Thai | `13` | Gibt an, dass der thailändische Kalender verwendet werden soll, wie er im königlichen Erlass Seiner Majestät König Vajiravudh (Rama VI.) in der Royal Gazette BE 2456 (1913 n. Chr.) und im Erlass des Premierministers Phibunsongkhram (1941 n. Chr.) festgelegt wurde, wonach das Jahr am gregorianischen 1. Januar beginnt und das Jahr Null dem gregorianischen Jahr 543 v. Chr. zugeordnet wird. |

## Beispiele

Zeigt, wie der Benutzer mit einem strukturierten Dokument-Tag zur Eingabe eines Datums aufgefordert wird.

```csharp
Document doc = new Document();

// Fügen Sie ein strukturiertes Dokument-Tag ein, das den Benutzer auffordert, ein Datum einzugeben.
// In Microsoft Word wird dieses Element als „Datumsauswahl-Inhaltssteuerelement“ bezeichnet.
// Wenn wir in Microsoft Word auf den Pfeil am rechten Ende dieses Tags klicken,
// Wir sehen ein Popup in Form eines anklickbaren Kalenders.
// Wir können dieses Popup verwenden, um ein Datum auszuwählen, das das Tag anzeigen soll.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Zeigt das Datum entsprechend der saudi-arabischen Landeseinstellung an.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Legen Sie das Format fest, in dem das Datum angezeigt werden soll.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Zeigt das Datum gemäß dem Hijri-Kalender an.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Bevor der Benutzer in Microsoft Word ein Datum auswählt, zeigt das Tag den Text „Klicken Sie hier, um ein Datum einzugeben.“ an.
// Legen Sie entsprechend dem Kalender des Tags die Eigenschaft „FullDate“ fest, damit das Tag ein Standarddatum anzeigt.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
