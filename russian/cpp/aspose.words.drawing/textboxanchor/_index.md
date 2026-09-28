---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. Указывает значения, используемые для вертикального выравнивания текста в фигуре в C++."
type: docs
weight: 39000
url: /ru/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


Указывает значения, используемые для вертикального выравнивания текста в фигуре.

```cpp
enum class TextBoxAnchor
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Верх | 0 | Текст выровнен по верхнему краю текстового поля. |
| Middle | 1 | Текст выровнен по середине текстового поля. |
| Низ | 2 | Текст выровнен по нижнему краю текстового поля. |
| TopCentered | 3 | Текст выровнен по верхнему центру текстового поля. |
| MiddleCentered | 4 | Текст выровнен по среднему центру текстового поля. |
| BottomCentered | 5 | Текст выровнен по нижнему центру текстового поля. |
| TopBaseline | 6 | Текст выровнен по верхней базовой линии текстового поля. |
| BottomBaseline | 7 | Текст выровнен по нижней базовой линии текстового поля. |
| TopCenteredBaseline | 8 | Текст выровнен по верхней центрированной базовой линии текстового поля. |
| BottomCenteredBaseline | 9 | Текст выровнен по нижней центрированной базовой линии текстового поля. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
