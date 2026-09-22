---
title: "Aspose::Words::Drawing::Shape::Shape yapıcı"
linktitle: "Shape"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Shape::Shape yapıcı. C++'ta yeni bir şekil nesnesi oluşturur."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


Yeni bir şekil nesnesi oluşturur.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| doküman | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Sahip belge. |
| shapeType | Aspose::Words::Drawing::ShapeType | Oluşturulacak şeklin türü. |
## Açıklamalar


Bir şekil oluşturduktan sonra istediğiniz şekil özelliklerini belirtmelisiniz.

## Örnekler



Yerel dosya sisteminden bir görüntü içeren şeklin bir belgeye nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// \"Shape\" sınıfının genel yapıcı yöntemi, \"ShapeMarkupLanguage.Vml\" işaretleme türüyle bir şekil oluşturur.
// Eğer SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped gibi ilkel olmayan bir türde şekil oluşturmanız gerekiyorsa,
// TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, veya DiagonalCornersRounded,
// lütfen DocumentBuilder.InsertShape yöntemini kullanın.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
