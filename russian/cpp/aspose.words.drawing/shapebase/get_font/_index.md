---
title: "Aspose::Words::Drawing::ShapeBase::get_Font метод"
linktitle: "get_Font"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Font метод. Предоставляет доступ к форматированию шрифта этого объекта в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words.drawing/shapebase/get_font/
---
## ShapeBase::get_Font method


Предоставляет доступ к форматированию шрифта этого объекта.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::ShapeBase::get_Font()
```


## Примеры



Показывает, как вставить текстовое поле и задать шрифт его содержимого.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 50);
builder->MoveTo(shape->get_LastParagraph());
builder->Write(u"This text is inside the text box.");

// Установите свойство \"Hidden\" объекта \"Font\" формы в \"true\", чтобы скрыть текстовое поле от глаз.
// и сократите пространство, которое он обычно занимает.
// Установите свойство \"Hidden\" объекта \"Font\" формы в \"false\", чтобы оставить текстовое поле видимым.
shape->get_Font()->set_Hidden(hideShape);

// Если форма видима, мы изменим её внешний вид через объект шрифта.
if (!hideShape)
{
    shape->get_Font()->set_HighlightColor(System::Drawing::Color::get_LightGray());
    shape->get_Font()->set_Color(System::Drawing::Color::get_Red());
    shape->get_Font()->set_Underline(Aspose::Words::Underline::Dash);
}

// Переместите построитель из текстового поля обратно в основной документ.
builder->MoveTo(shape->get_ParentParagraph());

builder->Writeln(u"\nThis text is outside the text box.");

doc->Save(get_ArtifactsDir() + u"Shape.Font.docx");
```

## См. также

* Class [Font](../../../aspose.words/font/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
