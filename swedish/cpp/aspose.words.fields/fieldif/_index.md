---
title: "Aspose::Words::Fields::FieldIf klass"
linktitle: "FieldIf"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIf klass. Implementerar IF-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 54000
url: /sv/cpp/aspose.words.fields/fieldif/
---
## FieldIf class


Implementerar IF-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIf : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [EvaluateCondition](./evaluatecondition/)() | Utvärderar villkoret. |
| [get_ComparisonOperator](./get_comparisonoperator/)() | Hämtar eller anger jämförelseoperatorn. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](./get_end/)() override | Hämtar noden som representerar fältets slut. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FalseText](./get_falsetext/)() | Hämtar eller anger den text som visas om jämförelseuttrycket är **false**. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LeftExpression](./get_leftexpression/)() | Hämtar eller anger den vänstra delen av jämförelseuttrycket. |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_RightExpression](./get_rightexpression/)() | Hämtar eller anger den högra delen av jämförelseuttrycket. |
| [get_Separator](./get_separator/)() override | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](./get_start/)() override | Hämtar noden som representerar fältets början. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_TrueText](./get_truetext/)() | Hämtar eller anger den text som visas om jämförelseuttrycket är true. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_ComparisonOperator](./set_comparisonoperator/)(const System::String\&) | Inställningsmetod för [Aspose::Words::Fields::FieldIf::get_ComparisonOperator](./get_comparisonoperator/). |
| [set_FalseText](./set_falsetext/)(const System::String\&) | Inställningsmetod för [Aspose::Words::Fields::FieldIf::get_FalseText](./get_falsetext/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftExpression](./set_leftexpression/)(const System::String\&) | Inställningsmetod för [Aspose::Words::Fields::FieldIf::get_LeftExpression](./get_leftexpression/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightExpression](./set_rightexpression/)(const System::String\&) | Inställningsmetod för [Aspose::Words::Fields::FieldIf::get_RightExpression](./get_rightexpression/). |
| [set_TrueText](./set_truetext/)(const System::String\&) | Inställningsmetod för [Aspose::Words::Fields::FieldIf::get_TrueText](./get_truetext/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Anmärkningar


Jämför värdena som anges av uttrycken [LeftExpression](./get_leftexpression/) och [RightExpression](./get_rightexpression/) med hjälp av operatorn som anges av [ComparisonOperator](./get_comparisonoperator/).

Ett fält i följande format kommer att användas som en källa för kopplad utskrift: { IF 0 = 0 "{PatientsNameFML}" "" \* MERGEFORMAT }

## Exempel



Visar hur man infogar ett IF-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// IF-fältet kommer att visa en sträng från antingen dess \"TrueText\"-egenskap,
// eller dess \"FalseText\"-egenskap, beroende på sanningen i det påstående som vi har konstruerat.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// I det här fallet är \"0 = 1\" felaktigt, så det visade resultatet blir \"False\".
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

// Den här gången är påståendet korrekt, så det visade resultatet blir \"True\".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
