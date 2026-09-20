---
title: "Aspose::Words::Fields::FieldDocVariable::get_VariableName метод"
linktitle: "get_VariableName"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldDocVariable::get_VariableName метод. Получает или задает имя переменной документа, которое следует получить, в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


Получает или задает имя переменной документа для получения.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## Примеры



Показывает, как использовать поля DOCPROPERTY для отображения свойств документа и переменных.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два способа использования полей DOCPROPERTY.
// 1 -  Показать встроенное свойство:
// Установите пользовательское значение для встроенного свойства "Category", затем вставьте поле DOCPROPERTY, которое ссылается на него.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Показать пользовательскую переменную документа:
// Определите пользовательскую переменную, затем ссылаться на неё с помощью поля DOCPROPERTY.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## См. также

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
