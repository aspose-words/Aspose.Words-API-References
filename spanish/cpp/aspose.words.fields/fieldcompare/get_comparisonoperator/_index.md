---
title: "Aspose::Words::Fields::FieldCompare::get_ComparisonOperator método"
linktitle: "get_ComparisonOperator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldCompare::get_ComparisonOperator method. Obtiene o establece el operador de comparación en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldcompare/get_comparisonoperator/
---
## FieldCompare::get_ComparisonOperator method


Obtiene o establece el operador de comparación.

```cpp
System::String Aspose::Words::Fields::FieldCompare::get_ComparisonOperator()
```


## Ejemplos



Muestra cómo comparar expresiones usando un campo COMPARE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"3");
field->set_ComparisonOperator(u"<");
field->set_RightExpression(u"2");
field->Update();

// El campo COMPARE muestra un "0" o un "1", dependiendo de la veracidad de su declaración.
// El resultado de esta declaración es falso, por lo que este campo mostrará un "0".
ASSERT_EQ(u" COMPARE  3 < 2", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

builder->Writeln();

field = System::ExplicitCast<Aspose::Words::Fields::FieldCompare>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldCompare, true));
field->set_LeftExpression(u"5");
field->set_ComparisonOperator(u"=");
field->set_RightExpression(u"2 + 3");
field->Update();

// Este campo muestra un "1" ya que la declaración es verdadera.
ASSERT_EQ(u" COMPARE  5 = \"2 + 3\"", field->GetFieldCode());
ASSERT_EQ(u"1", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.COMPARE.docx");
```

## Ver también

* Class [FieldCompare](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
