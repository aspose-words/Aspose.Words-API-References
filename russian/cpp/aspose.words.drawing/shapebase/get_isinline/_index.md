---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline метод"
linktitle: "get_IsInline"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline метод. Быстрый способ определить, находится ли эта фигура в строке текста в C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


Быстрый способ определить, позиционирована ли эта фигура в строке с текстом.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## Примечания


Имеет эффект только для фигур верхнего уровня.

## Примеры



Показывает, как определить, является ли фигура встроенной или плавающей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ниже представлены два типа обтекания, которые могут иметь формы.
// 1 -  Встроенная:
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// Встроенная фигура находится внутри абзаца среди других элементов абзаца, таких как фрагменты текста.
// В Microsoft Word мы можем щёлкнуть и перетащить фигуру в любой абзац, как если бы это был символ.
// Если фигура большая, она будет влиять на вертикальное расстояние между абзацами.
// Мы не можем переместить эту фигуру в место без абзаца.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  Плавающий:
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// Плавающая фигура принадлежит абзацу, в который мы её вставляем,
// который мы можем определить по символу привязки, появляющемуся при щелчке по фигуре.
// Если у фигуры слева нет видимого символа привязки,
// нам потребуется включить видимые привязки через "Options" -> "Display" -> "Object Anchors".
// В Microsoft Word мы можем щелкнуть левой кнопкой мыши и свободно перетаскивать эту фигуру в любое место.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
