---
title: "Aspose::Words::Fields::FieldSection class"
linktitle: "FieldSection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldSection Klasse. Implementiert das SECTION-Feld. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 88000
url: /de/cpp/aspose.words.fields/fieldsection/
---
## FieldSection class


Implementiert das SECTION-Feld. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldSection : public Aspose::Words::Fields::Field
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



Zeigt, wie man die Felder SECTION und SECTIONPAGES verwendet, um Seiten nach Abschnitten zu nummerieren.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Ein SECTION-Feld zeigt die Nummer des Abschnitts an, in dem es sich befindet.
builder->Write(u"Section ");
auto fieldSection = System::ExplicitCast<Aspose::Words::Fields::FieldSection>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSection, true));

ASSERT_EQ(u" SECTION ", fieldSection->GetFieldCode());

// Ein PAGE-Feld zeigt die Nummer der Seite an, in der es sich befindet.
builder->Write(u"\nPage ");
auto fieldPage = System::ExplicitCast<Aspose::Words::Fields::FieldPage>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, true));

ASSERT_EQ(u" PAGE ", fieldPage->GetFieldCode());

// Ein SECTIONPAGES-Feld zeigt die Anzahl der Seiten an, die der Abschnitt, in dem es sich befindet, umfasst.
builder->Write(u" of ");
auto fieldSectionPages = System::ExplicitCast<Aspose::Words::Fields::FieldSectionPages>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSectionPages, true));

ASSERT_EQ(u" SECTIONPAGES ", fieldSectionPages->GetFieldCode());

// Verlassen Sie die Kopfzeile und kehren Sie zum Hauptdokument zurück, um zwei Seiten einzufügen.
// Alle diese Seiten werden im ersten Abschnitt sein. Unsere Felder, die in jeder Kopfzeile einmal erscheinen,
// nummerieren die aktuellen/gesamten Seiten dieses Abschnitts.
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Wir können mit dem Document Builder einen neuen Abschnitt wie folgt einfügen.
// Dies wirkt sich auf die in den Feldern SECTION und SECTIONPAGES in allen kommenden Kopfzeilen angezeigten Werte aus.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

// Das PAGE-Feld wird die Seiten im gesamten Dokument weiterzählen.
// Wir können seinen Zähler in jedem Abschnitt manuell zurücksetzen, um die Seiten abschnittsweise zu verfolgen.
builder->get_CurrentSection()->get_PageSetup()->set_RestartPageNumbering(true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SECTION.SECTIONPAGES.docx");
```

## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
