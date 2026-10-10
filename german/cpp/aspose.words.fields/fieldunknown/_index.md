---
title: "Aspose::Words::Fields::FieldUnknown Klasse"
linktitle: "FieldUnknown"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldUnknown Klasse. Implementiert ein unbekanntes oder nicht erkanntes Feld. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 106000
url: /de/cpp/aspose.words.fields/fieldunknown/
---
## FieldUnknown class


Implementiert ein unbekanntes oder nicht erkanntes Feld. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldUnknown : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](./get_end/)() override | Liefert den Knoten, der das Feldende darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](./get_separator/)() override | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](./get_start/)() override | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |

## Beispiele



Zeigt, wie man mit dem Feld 'FieldNone' in einem Dokument arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Feld ein, das in seinem Feldcode keinen objektiven Feldtyp bezeichnet.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" NOTAREALFIELD //a");

// Der Feldtyp "FieldNone" ist für solche Felder reserviert.
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldNone, field->get_Type());

// Wir können weiterhin mit diesen Feldern arbeiten und sie als Instanzen der FieldUnknown Klasse zuweisen.
auto fieldUnknown = System::ExplicitCast<Aspose::Words::Fields::FieldUnknown>(field);
ASSERT_EQ(u" NOTAREALFIELD //a", fieldUnknown->GetFieldCode());
```

## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
