---
title: "Método get_VariableName de Aspose::Words::Fields::FieldDocVariable"
linktitle: "get_VariableName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_VariableName de Aspose::Words::Fields::FieldDocVariable. Obtiene o establece el nombre de la variable del documento a recuperar en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


Obtiene o establece el nombre de la variable del documento a recuperar.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## Ejemplos



Muestra cómo usar campos DOCPROPERTY para mostrar propiedades del documento y variables.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan dos formas de usar campos DOCPROPERTY.
// 1 -  Mostrar una propiedad incorporada:
// Establezca un valor personalizado para la propiedad incorporada "Category", luego inserte un campo DOCPROPERTY que lo referencie.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Mostrar una variable de documento personalizada:
// Defina una variable personalizada, luego haga referencia a esa variable con un campo DOCPROPERTY.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## Ver también

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
