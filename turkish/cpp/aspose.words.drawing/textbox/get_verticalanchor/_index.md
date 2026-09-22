---
title: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor yöntemi"
linktitle: "get_VerticalAnchor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor yöntemi. C++'ta bir şekil içinde metnin dikey hizalamasını belirtir."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


Bir şekil içinde metnin dikey hizalamasını belirtir.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## Açıklamalar


Varsayılan değer [Top](../../textboxanchor/).

## Örnekler



Bir metin kutusunun metin içeriğini dikey olarak nasıl hizalayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Top\" olarak ayarlayın
// bu metin kutusundaki metni şeklin üst tarafına hizalayın.
// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Middle\" olarak ayarlayın
// bu metin kutusundaki metni şeklin ortasına hizalayın.
// \"VerticalAnchor\" özelliğini \"TextBoxAnchor.Bottom\" olarak ayarlayın
// bu metin kutusundaki metni şeklin altına hizalayın.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Metin kutularının içindeki metnin dikey hizalanması Microsoft Word 2007 ve sonrasında kullanılabilir.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Ayrıca Bakınız

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
