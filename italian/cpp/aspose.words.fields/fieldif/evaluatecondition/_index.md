---
title: "Metodo Aspose::Words::Fields::FieldIf::EvaluateCondition"
linktitle: "EvaluateCondition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fields::FieldIf::EvaluateCondition. Valuta la condizione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldif/evaluatecondition/
---
## FieldIf::EvaluateCondition method


Valuta la condizione.

```cpp
Aspose::Words::Fields::FieldIfComparisonResult Aspose::Words::Fields::FieldIf::EvaluateCondition()
```


### ReturnValue

Un valore [FieldIfComparisonResult](../../fieldifcomparisonresult/) che rappresenta il risultato della valutazione della condizione.

## Esempi



Mostra come inserire un campo IF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// Il campo IF visualizzerà una stringa dalla proprietà "TrueText",
// oppure dalla proprietà "FalseText", a seconda della verità dell'affermazione che abbiamo costruito.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// In questo caso, "0 = 1" è errato, quindi il risultato visualizzato sarà "False".
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

// Questa volta l'affermazione è corretta, quindi il risultato visualizzato sarà "True".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## Vedi anche

* Enum [FieldIfComparisonResult](../../fieldifcomparisonresult/)
* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
