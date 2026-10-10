---
title: "Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode metodu"
linktitle: "get_TextBoxWrapMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode metodu. Metnin bir şekil içinde nasıl sarıldığını C++'de belirler."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.drawing/textbox/get_textboxwrapmode/
---
## TextBox::get_TextBoxWrapMode method


Metnin bir şekil içinde nasıl kaydırılacağını belirler.

```cpp
Aspose::Words::Drawing::TextBoxWrapMode Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode()
```

## Açıklamalar


Varsayılan değer [Square](../../textboxwrapmode/).

## Örnekler



Bir metin kutusunun içeriği için sarma modunun nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// "TextBoxWrapMode" özelliğini "TextBoxWrapMode.None" olarak ayarlayarak metin kutusunun genişliğini artırın
// metni sığdırmak için, yeterince büyük olmalıdır.
// "TextBoxWrapMode" özelliğini "TextBoxWrapMode.Square" olarak ayarlayarak
// metin kutusunun içindeki tüm metni, boyutlarını koruyarak sarar.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## Ayrıca Bakınız

* Enum [TextBoxWrapMode](../../textboxwrapmode/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
