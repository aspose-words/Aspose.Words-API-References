---
title: "Aspose::Words::Fields::FieldIf::get_RightExpression metod"
linktitle: "get_RightExpression"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIf::get_RightExpression metod. Hämtar eller anger den högra delen av jämförelseuttrycket i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.fields/fieldif/get_rightexpression/
---
## FieldIf::get_RightExpression method


Hämtar eller anger den högra delen av jämförelseuttrycket.

```cpp
System::String Aspose::Words::Fields::FieldIf::get_RightExpression()
```


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

* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
