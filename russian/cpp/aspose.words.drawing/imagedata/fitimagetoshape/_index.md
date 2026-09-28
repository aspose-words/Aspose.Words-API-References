---
title: "Aspose::Words::Drawing::ImageData::FitImageToShape method"
linktitle: "FitImageToShape"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ImageData::FitImageToShape method. Подгоняет данные изображения к кадру Shape так, чтобы соотношение сторон данных изображения совпадало с соотношением сторон кадра Shape в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.drawing/imagedata/fitimagetoshape/
---
## ImageData::FitImageToShape method


Подгоняет данные изображения к кадру [Shape](../../shape/) так, чтобы соотношение сторон данных изображения совпадало с соотношением сторон кадра [Shape](../../shape/).

```cpp
void Aspose::Words::Drawing::ImageData::FitImageToShape()
```


## Примеры



Показывает, как подогнать данные изображения к кадру [Shape](../../shape/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте форму изображения и оставьте её ориентацию в состоянии по умолчанию.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 300, 450);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Barcode.png");
shape->get_ImageData()->FitImageToShape();

doc->Save(get_ArtifactsDir() + u"Shape.FitImageToShape.docx");
```

## См. также

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
