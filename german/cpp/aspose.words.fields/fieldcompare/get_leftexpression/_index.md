---
title: "Aspose::Words::Fields::FieldCompare::get_LeftExpression Methode"
linktitle: "get_LeftExpression"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldCompare::get_LeftExpression Methode. Ermittelt oder legt den linken Teil des Vergleichsausdrucks in C++ fest."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldcompare/get_leftexpression/
---
## FieldCompare::get_LeftExpression method


Liest oder setzt den linken Teil des Vergleichsausdrucks.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_LeftExpression()
```


## Beispiele



Zeigt, wie man Ausdrücke mit einem COMPARE-Feld vergleicht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// Das COMPARE-Feld zeigt eine "0" oder eine "1" an, abhängig von der Wahrheit seiner Anweisung.
// Das Ergebnis dieser Anweisung ist falsch, sodass dieses Feld eine "0" anzeigt.
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// Dieses Feld zeigt eine "1" an, da die Anweisung wahr ist.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## Siehe auch

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
