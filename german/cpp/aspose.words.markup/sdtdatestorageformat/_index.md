---
title: "Aspose::Words::Markup::SdtDateStorageFormat Enum"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::SdtDateStorageFormat enum. Gibt an, wie das Datum für ein Datums‑SDT gespeichert/abgerufen wird, wenn das SDT an einen XML‑Knoten im Datenspeicher des Dokuments in C++ gebunden ist."
type: docs
weight: 20000
url: /de/cpp/aspose.words.markup/sdtdatestorageformat/
---
## SdtDateStorageFormat enum


Gibt an, wie das Datum für ein Datums‑SDT gespeichert/abgerufen wird, wenn das SDT an einen XML‑Knoten im Datenspeicher des Dokuments gebunden ist.

```cpp
enum class SdtDateStorageFormat
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Datum | 0 | Der Datumswert für ein Datums‑SDT wird als Datum im Standard‑XML‑Schema‑Datumsformat gespeichert. |
| DateTime | 1 | Der Datumswert für ein Datums‑SDT wird als Datum im Standard‑XML‑Schema‑DateTime‑Format gespeichert. |
| Text | 2 | Der Datumswert für ein Datums‑SDT wird als Text gespeichert. |
| Default | n/a | Standardwert ist [DateTime](./) |


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
