---
title: "Aspose::Words::Story::get_FirstParagraph yöntemi"
linktitle: "get_FirstParagraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Story::get_FirstParagraph yöntemi. Hikayedeki ilk paragrafı C++'da alır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/story/get_firstparagraph/
---
## Story::get_FirstParagraph method


Hikayedeki ilk paragrafı alır.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_FirstParagraph() override
```


## Örnekler



Bir metin run'ını font özelliğini kullanarak nasıl biçimlendireceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


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

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
