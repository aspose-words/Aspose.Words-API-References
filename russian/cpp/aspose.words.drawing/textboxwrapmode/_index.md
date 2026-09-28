---
title: "Перечисление Aspose::Words::Drawing::TextBoxWrapMode"
linktitle: "TextBoxWrapMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Drawing::TextBoxWrapMode. Указывает, как текст обтекает внутри формы в C++."
type: docs
weight: 40000
url: /ru/cpp/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enum


Указывает, как текст обтекает внутри фигуры.

```cpp
enum class TextBoxWrapMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Square | 0 | Текст обтекает внутри формы. |
| None | 2 | Текст не обтекает внутри формы. |


## Примеры



Показывает, как установить режим обтекания для содержимого текстового поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Установите свойство "TextBoxWrapMode" в "TextBoxWrapMode.None", чтобы увеличить ширину текстового поля
// чтобы разместить текст, если он будет достаточно большим.
// Установите свойство "TextBoxWrapMode" в "TextBoxWrapMode.Square", чтобы
// обернуть весь текст внутри текстового поля, сохраняя его размеры.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
