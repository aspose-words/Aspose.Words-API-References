---
title: "Aspose::Words::Drawing::TextBoxWrapMode enum"
linktitle: "TextBoxWrapMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextBoxWrapMode enum. Metnin C++'da bir şekil içinde nasıl sarıldığını belirtir."
type: docs
weight: 40000
url: /tr/cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


Metnin bir şekil içinde nasıl kaydırıldığını belirtir.

```cpp
enum class TextBoxWrapMode
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Square | 0 | Metin bir şekil içinde sarılır. |
| None | 2 | Metin bir şekil içinde sarılmaz. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
