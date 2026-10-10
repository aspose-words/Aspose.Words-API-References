---
title: "Aspose::Words::Fields::FieldIf::get_RightExpression Methode"
linktitle: "get_RightExpression"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldIf::get_RightExpression Methode. Gibt den rechten Teil des Vergleichsausdrucks zurück oder setzt ihn in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.fields/fieldif/get_rightexpression/
---
## FieldIf::get_RightExpression method


Liest oder setzt den rechten Teil des Vergleichsausdrucks.

```cpp
System::String Aspose::Words::Fields::FieldIf::get_RightExpression()
```


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

* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
