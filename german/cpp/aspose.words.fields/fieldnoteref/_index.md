---
title: "Aspose::Words::Fields::FieldNoteRef Klasse"
linktitle: "FieldNoteRef"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldNoteRef class. Implementiert das NOTEREF-Feld. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 72000
url: /de/cpp/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class


Implementiert das NOTEREF-Feld. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldNoteRef : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Ermittelt den Namen des Lesezeichens. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Ermittelt, ob ein Hyperlink zum markierten Absatz eingefügt werden soll. |
| [get_InsertReferenceMark](./get_insertreferencemark/)() | Fügt das Referenzzeichen mit derselben Zeichenformatierung wie der Fußnoten‑Referenz‑ oder Endnoten‑Referenz‑Stil ein. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Ermittelt, ob eine relative Position des markierten Absatzes eingefügt werden soll. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_Separator](../field/get_separator/)() | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Setzt den Namen des Lesezeichens. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Legt fest, ob ein Hyperlink zum markierten Absatz eingefügt werden soll. |
| [set_InsertReferenceMark](./set_insertreferencemark/)(bool) | Fügt das Referenzzeichen mit derselben Zeichenformatierung wie der Fußnoten‑Referenz‑ oder Endnoten‑Referenz‑Stil ein. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Legt fest, ob eine relative Position des markierten Absatzes eingefügt werden soll. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |

## Beispiele



Zeigt, wie Fußnoten mit dem NOTEREF‑Feld querverweist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"CrossReference: ");

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldNoteRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNoteRef, false));
// <--- Feld nicht aktualisieren
field->set_BookmarkName(u"CrossRefBookmark");
field->set_InsertHyperlink(true);
field->set_InsertReferenceMark(true);
field->set_InsertRelativePosition(false);
builder->Writeln();

builder->StartBookmark(u"CrossRefBookmark");
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Cross referenced footnote.");
builder->EndBookmark(u"CrossRefBookmark");
builder->Writeln();

doc->UpdateFields();

// Dieses Feld funktioniert nur in älteren Versionen von Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Field.NOTEREF.doc");
```

## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
