---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition"
linktitle: "get_RelativeHorizontalPosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition. Указывает, относительно чего позиционируется фигура по горизонтали в C++."
type: docs
weight: 42000
url: /ru/cpp/aspose.words.drawing/shapebase/get_relativehorizontalposition/
---
## ShapeBase::get_RelativeHorizontalPosition method


Указывает, относительно чего фигура позиционируется по горизонтали.

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalPosition()
```

## Примечания


Значение по умолчанию — [Column](../../relativehorizontalposition/).

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

* Enum [RelativeHorizontalPosition](../../relativehorizontalposition/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
