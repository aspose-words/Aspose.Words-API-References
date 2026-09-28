---
title: "Aspose::Words::Drawing::TextBox::get_FitShapeToText метод"
linktitle: "get_FitShapeToText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::TextBox::get_FitShapeToText метод. Определяет, будет ли Microsoft Word увеличивать форму, чтобы разместить текст, в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


Определяет, будет ли Microsoft Word увеличивать форму, чтобы вместить текст.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## Примечания


Значение по умолчанию — **false**.

## Примеры



Показывает, как заставить текстовое поле автоматически изменять размер, плотно охватывая своё содержимое.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Примените эти значения к обоим членам, чтобы родительская фигура подгонялась
// плотно к текстовому содержимому, игнорируя заданные размеры.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## См. также

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
