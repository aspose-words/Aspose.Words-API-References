---
title: "Aspose::Words::Drawing::TextBox::get_NoTextRotation метод"
linktitle: "get_NoTextRotation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::TextBox::get_NoTextRotation метод. Получает или задает логическое значение, указывающее, что текст в TextBox не должен вращаться при повороте фигуры в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.drawing/textbox/get_notextrotation/
---
## TextBox::get_NoTextRotation method


Получает или задает логическое значение, указывающее, что текст в [TextBox](../) не должен вращаться при повороте фигуры.

```cpp
bool Aspose::Words::Drawing::TextBox::get_NoTextRotation()
```

## Примечания


Значение по умолчанию — **false**

## Примеры



Показывает, как отключить вращение текста, когда фигура вращается.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Ellipse, 20, 20);
shape->get_TextBox()->set_NoTextRotation(true);

doc->Save(get_ArtifactsDir() + u"Shape.NoTextRotation.docx");
```

## См. также

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
