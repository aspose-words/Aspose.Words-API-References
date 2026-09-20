---
title: "Aspose::Words::Drawing::Shape::get_FirstParagraph метод"
linktitle: "get_FirstParagraph"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Shape::get_FirstParagraph метод. Получает первый абзац в форме в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.drawing/shape/get_firstparagraph/
---
## Shape::get_FirstParagraph method


Получает первый абзац в фигуре.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_FirstParagraph()
```


## Примеры



Показывает, как создать и отформатировать текстовое поле.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте плавающее текстовое поле.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// Установите горизонтальное и вертикальное выравнивание текста внутри фигуры.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// Добавьте абзац в текстовое поле и добавьте последовательность текста, которую будет отображать текстовое поле.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## См. также

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
