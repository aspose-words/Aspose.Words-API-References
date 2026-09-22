---
title: "Aspose::Words::Drawing::Shape::get_TextBox yöntemi"
linktitle: "get_TextBox"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Shape::get_TextBox yöntemi. C++'ta bir şekilde metnin nasıl görüntüleneceğini belirten öznitelikleri tanımlar."
type: docs
weight: 24000
url: /tr/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


Metnin bir şekil içinde nasıl görüntüleneceğini belirten öznitelikleri tanımlar.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
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

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
