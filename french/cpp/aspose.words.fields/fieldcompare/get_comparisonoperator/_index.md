---
title: "Aspose::Words::Fields::FieldCompare::get_ComparisonOperator méthode"
linktitle: "get_ComparisonOperator"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FieldCompare::get_ComparisonOperator méthode. Obtient ou définit l'opérateur de comparaison en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.fields/fieldcompare/get_comparisonoperator/
---
## FieldCompare::get_ComparisonOperator method


Obtient ou définit l'opérateur de comparaison.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_ComparisonOperator()
```


## Exemples



Montre comment comparer des expressions en utilisant un champ COMPARE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// Le champ COMPARE affiche un "0" ou un "1", selon la véracité de son énoncé.
// Le résultat de cet énoncé est faux, de sorte que ce champ affichera un "0".
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// Ce champ affiche un "1" puisque l'énoncé est vrai.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## Voir aussi

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
