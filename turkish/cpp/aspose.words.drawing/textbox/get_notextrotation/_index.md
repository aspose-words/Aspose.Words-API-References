---
title: "Aspose::Words::Drawing::TextBox::get_NoTextRotation yöntemi"
linktitle: "get_NoTextRotation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextBox::get_NoTextRotation yöntemi. C++'ta şekil döndürüldüğünde TextBox içindeki metnin dönmemesi gerektiğini belirten bir boolean değer alır veya ayarlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


Şekil döndürüldüğünde [TextBox](../) içindeki metnin dönmemesi gerektiğini belirten bir boolean değer alır veya ayarlar.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## Açıklamalar


Varsayılan değer **false**

## Örnekler



Şekil döndürüldüğünde metin döndürmeyi nasıl devre dışı bırakacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## Ayrıca Bakınız

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
