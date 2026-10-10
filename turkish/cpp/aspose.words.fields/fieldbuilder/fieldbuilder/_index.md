---
title: "Aspose::Words::Fields::FieldBuilder::FieldBuilder yapıcı"
linktitle: "FieldBuilder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fields::FieldBuilder::FieldBuilder yapıcı. C++'ta FieldBuilder sınıfının bir örneğini başlatır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder::FieldBuilder constructor


Bir [FieldBuilder](../) sınıfının örneğini başlatır.

```cpp
Aspose::Words::Fields::FieldBuilder::FieldBuilder(Aspose::Words::Fields::FieldType fieldType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fieldType | Aspose::Words::Fields::FieldType | Oluşturulacak alanın türü. |

## Örnekler



Bir alan oluşturucu kullanarak bir alanın nasıl oluşturulup ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Bir belgeye metin içeriği eklemenin pratik bir yolu belge oluşturucu kullanmaktır.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u" Hello world! This text is one Run, which is an inline node.");

// Alanların kendi oluşturucuları vardır; bunları alan kodunu parça parça oluşturmak için de kullanabiliriz.
// Bu durumda, ABD posta kodunu temsil eden bir BARCODE alanı oluşturacağız,
// ve ardından bunu bir Run'un önüne ekleyeceğiz.
auto fieldBuilder = System::MakeObject<Aspose::Words::Fields::FieldBuilder>(Aspose::Words::Fields::FieldType::FieldBarcode);
fieldBuilder->AddArgument(u"90210");
fieldBuilder->AddSwitch(u"\\f", u"A");
fieldBuilder->AddSwitch(u"\\u");

fieldBuilder->BuildAndInsert(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.CreateWithFieldBuilder.docx");
```

## Ayrıca Bakınız

* Enum [FieldType](../../fieldtype/)
* Class [FieldBuilder](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
