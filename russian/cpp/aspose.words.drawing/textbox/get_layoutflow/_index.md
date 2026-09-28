---
title: "Aspose::Words::Drawing::TextBox::get_LayoutFlow метод"
linktitle: "get_LayoutFlow"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::TextBox::get_LayoutFlow метод. Определяет поток расположения текста в фигуре в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


Определяет поток размещения текста в форме.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## Примечания


Значение по умолчанию — [Horizontal](../../layoutflow/).

## Примеры



Показывает, как задать ориентацию текста внутри текстового поля.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// Переместите построитель документа внутрь TextBox и добавьте текст.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// Установите свойство "LayoutFlow", чтобы задать ориентацию текстового содержимого этого текстового поля.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## См. также

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
