---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment"
linktitle: "get_VerticalAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment. Указывает, как фигура позиционируется вертикально в C++."
type: docs
weight: 53000
url: /ru/cpp/aspose.words.drawing/shapebase/get_verticalalignment/
---
## ShapeBase::get_VerticalAlignment method


Указывает, как фигура позиционируется вертикально.

```cpp
Aspose::Words::Drawing::VerticalAlignment Aspose::Words::Drawing::ShapeBase::get_VerticalAlignment()
```

## Примечания


Значение по умолчанию — [None](../../verticalalignment/).

Имеет эффект только для плавающих фигур верхнего уровня.

## Примеры



Показывает, как вставить плавающее изображение в центр страницы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте плавающее изображение, которое будет находиться позади перекрывающего текста, и выровняйте его по центру страницы.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
shape->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Center);

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPageCenter.docx");
```

## См. также

* Enum [VerticalAlignment](../../verticalalignment/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
