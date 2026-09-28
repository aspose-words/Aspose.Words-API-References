---
title: "Метод Aspose::Words::Drawing::Shape::get_TextBox"
linktitle: "get_TextBox"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Shape::get_TextBox. Определяет атрибуты, указывающие, как текст отображается в фигуре в C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


Определяет атрибуты, указывающие, как текст отображается в фигуре.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
```


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

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
