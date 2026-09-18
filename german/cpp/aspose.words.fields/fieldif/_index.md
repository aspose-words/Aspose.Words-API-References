---
title: "Aspose::Words::Fields::FieldIf Klasse"
linktitle: "FieldIf"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIf Klasse. Implementiert das IF-Feld. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 54000
url: /de/cpp/aspose.words.fields/fieldif/
---
## FieldIf class


Implementiert das IF-Feld. Weitere Informationen finden Sie im [Arbeiten mit Feldern](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldIf : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [EvaluateCondition](./evaluatecondition/)() | Bewertet die Bedingung. |
| [get_ComparisonOperator](./get_comparisonoperator/)() | Liest oder setzt den Vergleichsoperator. |
| [get_DisplayResult](../field/get_displayresult/)() | Liefert den Text, der das angezeigte Feldresultat darstellt. |
| [get_End](./get_end/)() override | Liefert den Knoten, der das Feldende darstellt. |
| [get_End](../field/get_end/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FalseText](./get_falsetext/)() | Liest oder setzt den angezeigten Text, wenn der Vergleichsausdruck **false** ist. |
| [get_FieldEnd](../field/get_fieldend/)() const | Liefert den Knoten, der das Feldende darstellt. |
| [get_FieldStart](../field/get_fieldstart/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Format](../field/get_format/)() | Liefert ein [FieldFormat](../fieldformat/) Objekt, das typisierten Zugriff auf die Formatierung des Feldes bietet. |
| [get_IsDirty](../field/get_isdirty/)() | Liefert oder setzt, ob das aktuelle Ergebnis des Feldes aufgrund anderer Änderungen am Dokument nicht mehr korrekt (veraltet) ist. |
| [get_IsLocked](../field/get_islocked/)() | Liefert oder setzt, ob das Feld gesperrt ist (soll sein Ergebnis nicht neu berechnen). |
| [get_LeftExpression](./get_leftexpression/)() | Liest oder setzt den linken Teil des Vergleichsausdrucks. |
| [get_LocaleId](../field/get_localeid/)() | Liefert oder setzt die LCID des Feldes. |
| [get_Result](../field/get_result/)() | Liefert oder setzt den Text, der zwischen dem Feldtrennzeichen und dem Feldende liegt. |
| [get_RightExpression](./get_rightexpression/)() | Liest oder setzt den rechten Teil des Vergleichsausdrucks. |
| [get_Separator](./get_separator/)() override | Liefert den Knoten, der das Feldtrennzeichen darstellt. Kann **null** sein. |
| [get_Start](./get_start/)() override | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_Start](../field/get_start/)() const | Liefert den Knoten, der den Beginn des Feldes darstellt. |
| [get_TrueText](./get_truetext/)() | Liest oder setzt den angezeigten Text, wenn der Vergleichsausdruck true ist. |
| virtual [get_Type](../field/get_type/)() const | Liefert den Microsoft‑Word-Feldtyp. |
| [GetFieldCode](../field/getfieldcode/)() | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). Sowohl Feldcode als auch Feldresultat von untergeordneten Feldern sind enthalten. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Gibt den Text zwischen Feldbeginn und Feldtrennzeichen zurück (oder Feldende, falls kein Trennzeichen vorhanden ist). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Entfernt das Feld aus dem Dokument. Gibt einen Knoten direkt nach dem Feld zurück. Wenn das Ende des Feldes das letzte Kind seines übergeordneten Knotens ist, gibt es den übergeordneten Absatz zurück. Wenn das Feld bereits entfernt wurde, gibt es **null** zurück. |
| [set_ComparisonOperator](./set_comparisonoperator/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIf::get_ComparisonOperator](./get_comparisonoperator/). |
| [set_FalseText](./set_falsetext/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIf::get_FalseText](./get_falsetext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Setter für [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftExpression](./set_leftexpression/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIf::get_LeftExpression](./get_leftexpression/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Setter für [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Setter für [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightExpression](./set_rightexpression/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIf::get_RightExpression](./get_rightexpression/). |
| [set_TrueText](./set_truetext/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldIf::get_TrueText](./get_truetext/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Führt das Entlinken des Feldes aus. |
| [Update](../field/update/)() | Führt das Aktualisieren des Feldes aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
| [Update](../field/update/)(bool) | Führt ein Feld-Update aus. Wirft eine Ausnahme, wenn das Feld bereits aktualisiert wird. |
## Hinweise


Vergleicht die durch die Ausdrücke [LeftExpression](./get_leftexpression/) und [RightExpression](./get_rightexpression/) festgelegten Werte, wobei der durch [ComparisonOperator](./get_comparisonoperator/) festgelegte Operator verwendet wird.

Ein Feld im folgenden Format wird als Datenquelle für den Seriendruck verwendet: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

## Beispiele



Zeigt, wie man ein IF-Feld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// Das IF-Feld zeigt eine Zeichenkette entweder aus seiner "TrueText"-Eigenschaft an,
// oder aus seiner "FalseText"-Eigenschaft, abhängig von der Wahrheit der von uns erstellten Anweisung.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// In diesem Fall ist "0 = 1" falsch, daher wird das angezeigte Ergebnis "False" sein.
ASSERT_EQ(u" IF  0 = 1 True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::False, field->EvaluateCondition());
ASSERT_EQ(u"False", field->get_Result());

builder->Write(u"\nStatement 2: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// Dieses Mal ist die Anweisung korrekt, daher wird das angezeigte Ergebnis "True" sein.
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## Siehe auch

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
