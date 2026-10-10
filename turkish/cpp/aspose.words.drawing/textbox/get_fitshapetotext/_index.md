---
title: "Aspose::Words::Drawing::TextBox::get_FitShapeToText yöntemi"
linktitle: "get_FitShapeToText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextBox::get_FitShapeToText yöntemi. Microsoft Word'ün şekli metne sığacak şekilde büyütüp büyütmeyeceğini C++'ta belirler."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


Microsoft Word'ün şekli metne sığdırmak için büyütüp büyütmeyeceğini belirler.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## Açıklamalar


Varsayılan değer **false**'tur.

## Örnekler



Bir metin kutusunun içeriğine sıkı bir şekilde sığacak şekilde kendini yeniden boyutlandırmasını nasıl sağlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Bu değerleri her iki üye için de uygulayarak üst şeklin sığmasını sağlayın
// metin içeriğinin etrafına sıkı bir şekilde, ayarladığımız boyutları göz ardı ederek.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## Ayrıca Bakınız

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
