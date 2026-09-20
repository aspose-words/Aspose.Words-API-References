---
title: "Aspose::Words::Drawing::TextBox class"
linktitle: "TextBox"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::TextBox class. Определяет атрибуты, которые указывают, как текст отображается внутри фигуры. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.drawing/textbox/
---
## TextBox class


Определяет атрибуты, указывающие, как текст отображается внутри фигуры. Чтобы узнать больше, посетите статью документации [Working with Shapes](https://docs.aspose.com/words/cpp/working-with-shapes/) .

```cpp
class TextBox : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [BreakForwardLink](./breakforwardlink/)() | Разрывает связь со следующим [TextBox](./). |
| [get_FitShapeToText](./get_fitshapetotext/)() | Определяет, будет ли Microsoft Word увеличивать форму, чтобы вместить текст. |
| [get_InternalMarginBottom](./get_internalmarginbottom/)() | Указывает внутренний нижний отступ в пунктах для формы. |
| [get_InternalMarginLeft](./get_internalmarginleft/)() | Указывает внутренний левый отступ в пунктах для формы. |
| [get_InternalMarginRight](./get_internalmarginright/)() | Указывает внутренний правый отступ в пунктах для формы. |
| [get_InternalMarginTop](./get_internalmargintop/)() | Указывает внутренний верхний отступ в пунктах для формы. |
| [get_LayoutFlow](./get_layoutflow/)() | Определяет поток размещения текста в форме. |
| [get_Next](./get_next/)() | Возвращает или задает [TextBox](./), который представляет следующий [TextBox](./) в последовательности фигур. |
| [get_NoTextRotation](./get_notextrotation/)() | Получает или задает логическое значение, указывающее, что текст [TextBox](./) не должен вращаться при повороте формы. |
| [get_Parent](./get_parent/)() const | Получает родительскую форму для [TextBox](./). |
| [get_Previous](./get_previous/)() | Возвращает [TextBox](./), который представляет предыдущий [TextBox](./) в последовательности фигур. |
| [get_TextBoxWrapMode](./get_textboxwrapmode/)() | Определяет, как текст обтекает внутри формы. |
| [get_VerticalAnchor](./get_verticalanchor/)() | Указывает вертикальное выравнивание текста внутри фигуры. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsValidLinkTarget](./isvalidlinktarget/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Определяет, может ли этот [TextBox](./) быть связан с целевым [TextBox](./). |
| [set_FitShapeToText](./set_fitshapetotext/)(bool) | Сеттер для [Aspose::Words::Drawing::TextBox::get_FitShapeToText](./get_fitshapetotext/). |
| [set_InternalMarginBottom](./set_internalmarginbottom/)(double) | Сеттер для [Aspose::Words::Drawing::TextBox::get_InternalMarginBottom](./get_internalmarginbottom/). |
| [set_InternalMarginLeft](./set_internalmarginleft/)(double) | Сеттер для [Aspose::Words::Drawing::TextBox::get_InternalMarginLeft](./get_internalmarginleft/). |
| [set_InternalMarginRight](./set_internalmarginright/)(double) | Сеттер для [Aspose::Words::Drawing::TextBox::get_InternalMarginRight](./get_internalmarginright/). |
| [set_InternalMarginTop](./set_internalmargintop/)(double) | Сеттер для [Aspose::Words::Drawing::TextBox::get_InternalMarginTop](./get_internalmargintop/). |
| [set_LayoutFlow](./set_layoutflow/)(Aspose::Words::Drawing::LayoutFlow) | Сеттер для [Aspose::Words::Drawing::TextBox::get_LayoutFlow](./get_layoutflow/). |
| [set_Next](./set_next/)(const System::SharedPtr\<Aspose::Words::Drawing::TextBox\>\&) | Сеттер для [Aspose::Words::Drawing::TextBox::get_Next](./get_next/). |
| [set_NoTextRotation](./set_notextrotation/)(bool) | Сеттер для [Aspose::Words::Drawing::TextBox::get_NoTextRotation](./get_notextrotation/). |
| [set_TextBoxWrapMode](./set_textboxwrapmode/)(Aspose::Words::Drawing::TextBoxWrapMode) | Сеттер для [Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode](./get_textboxwrapmode/). |
| [set_VerticalAnchor](./set_verticalanchor/)(Aspose::Words::Drawing::TextBoxAnchor) | Сеттер для [Aspose::Words::Drawing::TextBox::get_VerticalAnchor](./get_verticalanchor/). |
| static [Type](./type/)() |  |
## Примечания


Используйте свойство [TextBox](../shape/get_textbox/) для доступа к текстовым свойствам фигуры. Вы не создаёте экземпляры класса [TextBox](./) напрямую.

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
