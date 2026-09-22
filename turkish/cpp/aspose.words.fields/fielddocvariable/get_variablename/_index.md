---
title: "Aspose::Words::Fields::FieldDocVariable::get_VariableName yöntemi"
linktitle: "get_VariableName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldDocVariable::get_VariableName yöntemi. C++'ta alınacak belge değişkeninin adını alır veya ayarlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fielddocvariable/get_variablename/
---
## FieldDocVariable::get_VariableName method


Alınacak belge değişkeninin adını alır veya ayarlar.

```cpp
System::String Aspose::Words::Fields::FieldDocVariable::get_VariableName()
```


## Örnekler



DOCPROPERTY alanlarını belge özelliklerini ve değişkenlerini görüntülemek için nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda DOCPROPERTY alanlarını kullanmanın iki yolu verilmiştir.
// 1 -  Yerleşik bir özelliği görüntüle:
// "Category" yerleşik özelliği için özel bir değer ayarlayın, ardından ona başvuran bir DOCPROPERTY alanı ekleyin.
doc->get_BuiltInDocumentProperties()->set_Category(u"My category");

auto fieldDocProperty = System::ExplicitCast<Aspose::Words::Fields::FieldDocProperty>(builder->InsertField(u" DOCPROPERTY Category "));
fieldDocProperty->Update();

ASSERT_EQ(u" DOCPROPERTY Category ", fieldDocProperty->GetFieldCode());
ASSERT_EQ(u"My category", fieldDocProperty->get_Result());

builder->InsertParagraph();

// 2 -  Özel bir belge değişkenini görüntüle:
// Özel bir değişken tanımlayın, ardından bu değişkeni bir DOCPROPERTY alanı ile referans alın.
ASSERT_EQ(0, doc->get_Variables()->get_Count());
doc->get_Variables()->Add(u"My variable", u"My variable's value");

auto fieldDocVariable = System::ExplicitCast<Aspose::Words::Fields::FieldDocVariable>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldDocVariable, true));
fieldDocVariable->set_VariableName(u"My Variable");
fieldDocVariable->Update();

ASSERT_EQ(u" DOCVARIABLE  \"My Variable\"", fieldDocVariable->GetFieldCode());
ASSERT_EQ(u"My variable's value", fieldDocVariable->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.DOCPROPERTY.DOCVARIABLE.docx");
```

## Ayrıca Bakınız

* Class [FieldDocVariable](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
