---
title: "Aspose::Words::Fields::FieldIf::get_ComparisonOperator méthode"
linktitle: "get_ComparisonOperator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldIf::get_ComparisonOperator méthode. Obtient ou définit l'opérateur de comparaison en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.fields/fieldif/get_comparisonoperator/
---
## FieldIf::get_ComparisonOperator method


Obtient ou définit l'opérateur de comparaison.

```cpp
System::String Aspose::Words::Fields::FieldIf::get_ComparisonOperator()
```


## Exemples



Montre comment insérer un champ IF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Statement 1: ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldIf>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIf, true));
field->set_LeftExpression(u"0");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"1");

// Le champ IF affichera une chaîne provenant soit de sa propriété "TrueText",
// ou de sa propriété "FalseText", selon la véracité de l'expression que nous avons construite.
field->set_TrueText(u"True");
field->set_FalseText(u"False");
field->Update();

// Dans ce cas, "0 = 1" est incorrect, donc le résultat affiché sera "False".
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

// Cette fois, l'expression est correcte, donc le résultat affiché sera "True".
ASSERT_EQ(u" IF  5 = \"2 + 3\" True False", field->GetFieldCode());
ASSERT_EQ(Aspose::Words::Fields::FieldIfComparisonResult::True, field->EvaluateCondition());
ASSERT_EQ(u"True", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.IF.docx");
```

## Voir aussi

* Class [FieldIf](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
