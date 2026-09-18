---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType Methode"
linktitle: "get_CalendarType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType Methode. Gibt den Kalendertyp für dieses SDT an. Standard ist Default in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_calendartype/
---
## StructuredDocumentTag::get_CalendarType method


Gibt den Kalendertyp für dieses **SDT** an. Standard ist [Default](../../sdtcalendartype/)

```cpp
Aspose::Words::Markup::SdtCalendarType Aspose::Words::Markup::StructuredDocumentTag::get_CalendarType()
```

## Hinweise


Der Zugriff auf diese Eigenschaft funktioniert nur für den [Date](../../sdttype/) SDT‑Typ.

Für alle anderen SDT‑Typen wird eine Ausnahme auftreten.

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

* Enum [SdtCalendarType](../../sdtcalendartype/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
