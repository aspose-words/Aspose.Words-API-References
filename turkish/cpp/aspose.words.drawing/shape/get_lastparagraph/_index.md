---
title: "Aspose::Words::Drawing::Shape::get_LastParagraph yöntemi"
linktitle: "get_LastParagraph"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Shape::get_LastParagraph yöntemi. C++'ta şekildeki son paragrafı alır."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.drawing/shape/get_lastparagraph/
---
## Shape::get_LastParagraph method


Şekildeki son paragrafı alır.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_LastParagraph()
```


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

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
