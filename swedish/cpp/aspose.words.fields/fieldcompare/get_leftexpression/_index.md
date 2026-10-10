---
title: "Aspose::Words::Fields::FieldCompare::get_LeftExpression‑metod"
linktitle: "get_LeftExpression"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldCompare::get_LeftExpression‑metod. Hämtar eller anger den vänstra delen av jämförelseuttrycket i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldcompare/get_leftexpression/
---
## FieldCompare::get_LeftExpression method


Hämtar eller anger den vänstra delen av jämförelseuttrycket.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_LeftExpression()
```


## Exempel



Visar hur man jämför uttryck med ett COMPARE-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// COMPARE-fältet visar en "0" eller en "1", beroende på dess påståendes sanningsvärde.
// Resultatet av detta påstående är falskt så att detta fält kommer att visa en "0".
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// Detta fält visar en "1" eftersom påståendet är sant.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## Se även

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
