---
title: "Aspose::Words::Markup::SdtCalendarType-Enum"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::SdtCalendarType-Enum. Gibt die möglichen Kalendertypen an, die verwendet werden können, um CalendarType in einem Office Open XML‑Dokument in C++ zu spezifizieren."
type: docs
weight: 19000
url: /de/cpp/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enum


Gibt die möglichen Kalendertypen an, die verwendet werden können, um [CalendarType](../structureddocumenttag/get_calendartype/) in einem Office Open XML‑Dokument zu spezifizieren.

```cpp
enum class SdtCalendarType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Default | 0 | Wird als Standardwert in OOXML verwendet. Gleichbedeutend mit [Gregorian](./). |
| Gregorianisch | n/a | Gibt an, dass der Gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. Dieser Kalender sollte in die entsprechende Sprache lokalisiert werden. |
| GregorianArabic | n/a | Gibt an, dass der Gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. Die Werte dieses Kalenders sollten in Arabisch dargestellt werden. |
| GregorianMeFrench | n/a | Gibt an, dass der Gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. Die Werte für diesen Kalender sollten in Mittelostfranzösisch präsentiert werden. |
| GregorianUs | n/a | Gibt an, dass der Gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. Die Werte für diesen Kalender sollten auf Englisch dargestellt werden. |
| GregorianXlitEnglish | n/a | Gibt an, dass der Gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. Die Werte für diesen Kalender sollten die Darstellung der englischen Zeichenketten in den entsprechenden arabischen Zeichen sein (die arabische Transliteration des Englischen für den Gregorianischen Kalender). |
| GregorianXlitFrench | n/a | Gibt an, dass der Gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. Die Werte für diesen Kalender sollten die Darstellung der französischen Zeichenketten in den entsprechenden arabischen Zeichen sein (die arabische Transliteration des Französischen für den Gregorianischen Kalender). |
| Hebräisch | n/a | Gibt an, dass der hebräische Mondkalender, wie durch die Gaußsche Formel für das Passah [CITATION] und *The Complete Restatement of Oral Law* (Mishneh Torah) beschrieben, verwendet werden soll. |
| Hijri | n/a | Gibt an, dass der Hijri-Mondkalender, wie vom Königreich Saudi-Arabien, Ministerium für Islamische Angelegenheiten, Stiftungen, Da‘wah und Führung beschrieben, verwendet werden soll. |
| Japan | n/a | Gibt an, dass der japanische Kaiserzeit‑Kalender, wie im Japanischen Industrie‑Standard JIS X 0301 beschrieben, verwendet werden soll. |
| Korea | n/a | Gibt an, dass der koreanische Tangun‑Ära‑Kalender, wie im koreanischen Gesetzesbeschluss Nr. 4 beschrieben, verwendet werden soll. |
| Keine | n/a | Gibt an, dass kein Kalender verwendet werden soll. |
| Saka | n/a | Gibt an, dass der Saka‑Ära‑Kalender, wie vom Calendar Reform Committee of India, als Teil des Indian Ephemeris and Nautical Almanac, verwendet werden soll. |
| Taiwan | n/a | Gibt an, dass der taiwanesische Kalender, wie im chinesischen Nationalstandard CNS 7648 definiert, verwendet werden soll. |
| Thailändisch | n/a | Gibt an, dass der thailändische Kalender, wie durch das Königliche Dekret von H.M. König Vajiravudh (Rama VI) im Königlichen Amtsblatt B. E. 2456 (1913 n. Chr.) und durch das Dekret des Premierministers Phibunsongkhram (1941 n. Chr.) festgelegt, das Jahr am gregorianischen 1. Januar beginnen lässt und das Jahr Null auf das gregorianische Jahr 543 v. Chr. abbildet, verwendet werden soll. |


## Beispiele



Zeigt, wie der Benutzer aufgefordert wird, ein Datum mit einem strukturierten Dokument-Tag einzugeben.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Fügen Sie ein strukturiertes Dokument-Tag ein, das den Benutzer auffordert, ein Datum einzugeben.
// In Microsoft Word ist dieses Element als „Date picker content control“ bekannt.
// Wenn wir in Microsoft Word auf den Pfeil am rechten Ende dieses Tags klicken,
// sehen wir ein Popup in Form eines anklickbaren Kalenders.
// Wir können dieses Popup verwenden, um ein Datum auszuwählen, das das Tag anzeigen soll.
auto sdtDate = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Date, Aspose::Words::Markup::MarkupLevel::Inline);

// Zeigt das Datum gemäß dem saudi-arabischen Arabisch‑Locale an.
sdtDate->set_DateDisplayLocale(System::Globalization::CultureInfo::GetCultureInfo(u"ar-SA")->get_LCID());

// Legen Sie das Format fest, mit dem das Datum angezeigt wird.
sdtDate->set_DateDisplayFormat(u"dd MMMM, yyyy");
sdtDate->set_DateStorageFormat(Aspose::Words::Markup::SdtDateStorageFormat::DateTime);

// Zeigt das Datum gemäß dem Hijri‑Kalender an.
sdtDate->set_CalendarType(Aspose::Words::Markup::SdtCalendarType::Hijri);

// Bevor der Benutzer in Microsoft Word ein Datum auswählt, zeigt das Tag den Text "Click here to enter a date." an.
// Legen Sie gemäß dem Kalender des Tags die Eigenschaft "FullDate" fest, um das Tag ein Standarddatum anzeigen zu lassen.
sdtDate->set_FullDate(System::DateTime(1440, 10, 20));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(sdtDate);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Date.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
