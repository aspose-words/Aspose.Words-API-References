---
title: "Aspose::Words::Fields::FieldDdeAuto Klasse"
linktitle: "FieldDdeAuto"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldDdeAuto Klasse. Implementiert das DDEAUTO‑Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 33000
url: /de/cpp/aspose.words.fields/fieldddeauto/
---
## FieldDdeAuto class


Implementiert das DDEAUTO-Feld. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldDdeAuto : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Ermittelt, ob das verknüpfte Objekt als Bitmap eingefügt wird. |
| [get_InsertAsHtml](./get_insertashtml/)() | Ermittelt, ob das verknüpfte Objekt als HTML‑Text eingefügt wird. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Ermittelt, ob das verknüpfte Objekt als Bild eingefügt wird. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Ermittelt, ob das verknüpfte Objekt im Rich‑Text‑Format (RTF) eingefügt wird. |
| [get_InsertAsText](./get_insertastext/)() | Ermittelt, ob das verknüpfte Objekt im Nur‑Text‑Format eingefügt wird. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Ermittelt, ob das verknüpfte Objekt als Unicode‑Text eingefügt wird. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLinked](./get_islinked/)() | Ermittelt, ob die Dateigröße reduziert werden soll, indem Grafikdaten nicht im Dokument gespeichert werden. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_ProgId](./get_progid/)() | Ermittelt den Anwendungstyp der Linkinformationen. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_SourceFullName](./get_sourcefullname/)() | Ermittelt den Namen und den Speicherort der Quelldatei. |
| [get_SourceItem](./get_sourceitem/)() | Ermittelt den Teil der Quelldatei, der verlinkt wird. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Legt fest, ob das verknüpfte Objekt als Bitmap eingefügt werden soll. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Legt fest, ob das verknüpfte Objekt als HTML‑Formattierter Text eingefügt werden soll. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Legt fest, ob das verknüpfte Objekt als Bild eingefügt werden soll. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Legt fest, ob das verknüpfte Objekt im Rich‑Text‑Format (RTF) eingefügt werden soll. |
| [set_InsertAsText](./set_insertastext/)(bool) | Legt fest, ob das verknüpfte Objekt im Nur‑Text‑Format eingefügt werden soll. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Legt fest, ob das verknüpfte Objekt als Unicode‑Text eingefügt werden soll. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Legt fest, ob die Dateigröße reduziert werden soll, indem Grafikdaten nicht im Dokument gespeichert werden. |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Legt den Anwendungstyp der Linkinformationen fest. |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Legt den Namen und den Speicherort der Quelldatei fest. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Legt den Teil der Quelldatei fest, der verlinkt wird. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
