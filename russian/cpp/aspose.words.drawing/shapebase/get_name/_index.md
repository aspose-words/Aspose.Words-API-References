---
title: "Aspose::Words::Drawing::ShapeBase::get_Name метод"
linktitle: "get_Name"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Name метод. Получает или задает необязательное имя фигуры в C++."
type: docs
weight: 40000
url: /ru/cpp/aspose.words.drawing/shapebase/get_name/
---
## ShapeBase::get_Name method


Получает или задает необязательное имя фигуры.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Name()
```

## Примечания


По умолчанию — пустая строка.

Не может быть **null**, но может быть пустой строкой.

## Примеры



Показывает, как использовать альтернативный текст фигуры.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 150, 150);
shape->set_Name(u"MyCube");

shape->set_AlternativeText(u"Alt text for MyCube.");

// Мы можем получить доступ к альтернативному тексту фигуры, щёлкнув её правой кнопкой мыши, а затем через "Format AutoShape" -> "Alt Text".
doc->Save(get_ArtifactsDir() + u"Shape.AltText.docx");

// Сохраните документ в HTML, а затем удалите связанную изображение, принадлежащее нашей фигуре.
// Браузер, который читает наш HTML, отобразит альтернативный текст вместо отсутствующего изображения.
doc->Save(get_ArtifactsDir() + u"Shape.AltText.html");
System::IO::File::Delete(get_ArtifactsDir() + u"Shape.AltText.001.png");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
