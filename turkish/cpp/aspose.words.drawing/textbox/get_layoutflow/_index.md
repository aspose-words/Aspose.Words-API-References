---
title: "Aspose::Words::Drawing::TextBox::get_LayoutFlow metodu"
linktitle: "get_LayoutFlow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::TextBox::get_LayoutFlow metodu. C++'da bir şeklin metin yerleşim akışını belirler."
type: docs
weight: 8000
url: /tr/cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


Bir şekil içinde metin düzeninin akışını belirler.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## Açıklamalar


Varsayılan değer [Horizontal](../../layoutflow/)dır.

## Örnekler



Bir metin kutusunun içindeki metnin yönünü nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Belge oluşturucuyu TextBox içine taşıyın ve metin ekleyin.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// \"LayoutFlow\" özelliğini ayarlayarak bu metin kutusunun metin içeriği için bir yön belirleyin.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## Ayrıca Bakınız

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
