---
title: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel metodu"
linktitle: "get_IsTopLevel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel metodu. Bu şekil C++'ta bir grup şeklinin çocuğu değilse true döndürür."
type: docs
weight: 36000
url: /tr/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


Bu şekil bir grup şeklin çocuğu değilse **true** döndürür.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Örnekler



Bir şeklin bir grup şeklinin parçası olup olmadığını nasıl anlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Bir şekil varsayılan olarak herhangi bir grup şeklinin parçası değildir ve bu nedenle "IsTopLevel" özelliği "true" olarak ayarlanmıştır.
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Bir şekli bir grup şekline dahil ettiğimizde, "IsTopLevel" özelliği "false" olur.
ASSERT_FALSE(shape->get_IsTopLevel());
```

## Ayrıca Bakınız

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
