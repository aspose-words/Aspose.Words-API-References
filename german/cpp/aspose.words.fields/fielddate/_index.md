---
title: "Aspose::Words::Fields::FieldDate‑Klasse"
linktitle: "FieldDate"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldDate‑Klasse. Implementiert das DATE‑Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 31000
url: /de/cpp/aspose.words.fields/fielddate/
---
## FieldDate class


Implementiert das DATE-Feld. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldDate : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                  public Aspose::Words::Fields::IFieldWithCalendar
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [get_UseLastFormat](./get_uselastformat/)() | Ruft ab oder legt fest, ob beim Einfügen eines neuen DATE‑Felds ein vom Host‑Programm zuletzt verwendetes Format verwendet werden soll. |
| [get_UseLunarCalendar](./get_uselunarcalendar/)() override | Liest oder setzt, ob der islamische Mondkalender oder der hebräische Mondkalender verwendet wird. |
| [get_UseSakaEraCalendar](./get_usesakaeracalendar/)() override | Liest oder setzt, ob der Saka‑Eras‑Kalender verwendet wird. |
| [get_UseUmAlQuraCalendar](./get_useumalquracalendar/)() override | Liest oder setzt, ob der Um‑al‑Qura‑Kalender verwendet wird. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_UseLastFormat](./set_uselastformat/)(bool) | Setter für [Aspose::Words::Fields::FieldDate::get_UseLastFormat](./get_uselastformat/). |
| [set_UseLunarCalendar](./set_uselunarcalendar/)(bool) | Setter für [Aspose::Words::Fields::FieldDate::get_UseLunarCalendar](./get_uselunarcalendar/). |
| [set_UseSakaEraCalendar](./set_usesakaeracalendar/)(bool) | Setter für [Aspose::Words::Fields::FieldDate::get_UseSakaEraCalendar](./get_usesakaeracalendar/). |
| [set_UseUmAlQuraCalendar](./set_useumalquracalendar/)(bool) | Setter für [Aspose::Words::Fields::FieldDate::get_UseUmAlQuraCalendar](./get_useumalquracalendar/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |

## Beispiele



Zeigt, wie DATE‑Felder verwendet werden, um Daten gemäß verschiedener Kalenderarten anzuzeigen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn wir möchten, dass der Text im Dokument stets das korrekte Datum anzeigt, können wir ein DATE‑Feld verwenden.
// Im Folgenden sind drei Arten von Kulturkalendern aufgeführt, die ein DATE‑Feld zur Anzeige eines Datums verwenden kann.
// 1 -  Islamischer Mondkalender:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLunarCalendar(true);
ASSERT_EQ(u" DATE  \\h", field->GetFieldCode());
builder->Writeln();

// 2 -  Umm al‑Qura‑Kalender:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseUmAlQuraCalendar(true);
ASSERT_EQ(u" DATE  \\u", field->GetFieldCode());
builder->Writeln();

// 3 -  Indischer Nationalkalender:
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseSakaEraCalendar(true);
ASSERT_EQ(u" DATE  \\s", field->GetFieldCode());
builder->Writeln();

// Fügen Sie ein DATE‑Feld ein und setzen Sie dessen Kalendertyp auf den zuletzt vom Host‑Programm verwendeten.
// In Microsoft Word wird der Typ der zuletzt im Dialogfeld Einfügen → Text → Datum und Uhrzeit verwendet.
field = System::ExplicitCast<Aspose::Words::Fields::FieldDate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true));
field->set_UseLastFormat(true);
ASSERT_EQ(u" DATE  \\l", field->GetFieldCode());
builder->Writeln();

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.DATE.docx");
```

## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
