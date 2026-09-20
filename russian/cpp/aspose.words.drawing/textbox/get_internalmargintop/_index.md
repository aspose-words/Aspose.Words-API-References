---
title: "Aspose::Words::Drawing::TextBox::get_InternalMarginTop метод"
linktitle: "get_InternalMarginTop"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::TextBox::get_InternalMarginTop метод. Указывает внутренний верхний отступ в пунктах для фигуры в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.drawing/textbox/get_internalmargintop/
---
## TextBox::get_InternalMarginTop method


Указывает внутренний верхний отступ в пунктах для формы.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginTop()
```

## Примечания


Значение по умолчанию — 1/20 дюйма.

## Примеры



Показывает, как задать внутренние отступы для текстового поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте другое текстовое поле с определёнными отступами.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## См. также

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
