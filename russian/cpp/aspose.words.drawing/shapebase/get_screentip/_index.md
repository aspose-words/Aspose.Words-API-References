---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_ScreenTip"
linktitle: "get_ScreenTip"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_ScreenTip. Определяет текст, отображаемый при наведении указателя мыши на фигуру в C++."
type: docs
weight: 46000
url: /ru/cpp/aspose.words.drawing/shapebase/get_screentip/
---
## ShapeBase::get_ScreenTip method


Определяет текст, отображаемый при наведении указателя мыши на фигуру.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_ScreenTip()
```

## Примечания


Значение по умолчанию — пустая строка.

## Примеры



Показывает, как вставить фигуру, содержащую изображение, и также являющуюся гиперссылкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_HRef(u"https://forum.aspose.com/");
shape->set_Target(u"New Window");
shape->set_ScreenTip(u"Aspose.Words Support Forums");

// Ctrl + щелчок левой кнопкой мыши по фигуре в Microsoft Word откроет новое окно веб-браузера
// и перенесёт нас к гиперссылке в свойстве "HRef".
doc->Save(get_ArtifactsDir() + u"Image.InsertImageWithHyperlink.docx");
```

## См. также

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
