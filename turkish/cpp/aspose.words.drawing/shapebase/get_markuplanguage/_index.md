---
title: "Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage method"
linktitle: "get_MarkupLanguage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage yöntemi. Bu grafik nesnesi için kullanılan MarkupLanguage'i C++'da alır."
type: docs
weight: 39000
url: /tr/cpp/aspose.words.drawing/shapebase/get_markuplanguage/
---
## ShapeBase::get_MarkupLanguage method


Bu grafik nesnesi için kullanılan MarkupLanguage'ı alır.

```cpp
Aspose::Words::Drawing::ShapeMarkupLanguage Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage() const
```


## Örnekler



Bir şeklin boyutunu ve işaretleme dilini nasıl doğrulayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, shape->get_MarkupLanguage());
ASPOSE_ASSERT_EQ(System::Drawing::SizeF(300.0f, 300.0f), shape->get_SizeInPoints());
```

## Ayrıca Bakınız

* Enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
