---
title: "Aspose::Words::Drawing::Shape::get_FirstParagraph method"
linktitle: "get_FirstParagraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Shape::get_FirstParagraph method. Şeklin içindeki ilk paragrafı C++'da alır."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.drawing/shape/get_firstparagraph/
---
## Shape::get_FirstParagraph method


Şekildeki ilk paragrafı alır.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_FirstParagraph()
```


## Örnekler



Bir metin kutusunun nasıl oluşturulacağını ve biçimlendirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Yüzen bir metin kutusu oluştur.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Şeklin içindeki metnin yatay ve dikey hizalamasını ayarla.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Metin kutusuna bir paragraf ekle ve metin kutusunun göstereceği bir metin akışı ekle.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## Ayrıca Bakınız

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
