---
title: "Aspose::Words::Fields::FieldCompare::get_LeftExpression metodo"
linktitle: "get_LeftExpression"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldCompare::get_LeftExpression metodo. Ottiene o imposta la parte sinistra dell'espressione di confronto in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fields/fieldcompare/get_leftexpression/
---
## FieldCompare::get_LeftExpression method


Ottiene o imposta la parte sinistra dell'espressione di confronto.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_LeftExpression()
```


## Esempi



Mostra come confrontare le espressioni utilizzando un campo COMPARE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// Il campo COMPARE visualizza uno "0" o un "1", a seconda della verità della sua affermazione.
// Il risultato di questa affermazione è falso, quindi questo campo visualizzerà uno "0".
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// Questo campo visualizza un "1" poiché l'affermazione è vera.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## Vedi anche

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
