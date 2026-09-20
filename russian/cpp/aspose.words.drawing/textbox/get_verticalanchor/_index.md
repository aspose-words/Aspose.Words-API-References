---
title: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor метод"
linktitle: "get_VerticalAnchor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor метод. Указывает вертикальное выравнивание текста внутри фигуры в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


Указывает вертикальное выравнивание текста внутри фигуры.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## Примечания


Значение по умолчанию — [Top](../../textboxanchor/).

## Примеры



Показывает, как вертикально выровнять текстовое содержимое текстового поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Top", чтобы
// выравнять текст в этом текстовом поле по верхней стороне фигуры.
// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Middle", чтобы
// выравнять текст в этом текстовом поле по центру фигуры.
// Установите свойство "VerticalAnchor" в значение "TextBoxAnchor.Bottom", чтобы
// выравнять текст в этом текстовом поле по нижней части фигуры.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Вертикальное выравнивание текста внутри текстовых полей доступно, начиная с Microsoft Word 2007.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## См. также

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
