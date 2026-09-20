---
title: "Метод Aspose::Words::Drawing::ShapeBase::get_HRef"
linktitle: "get_HRef"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::ShapeBase::get_HRef. Получает или задает полный адрес гиперссылки для фигуры в C++."
type: docs
weight: 24000
url: /ru/cpp/aspose.words.drawing/shapebase/get_href/
---
## ShapeBase::get_HRef method


Получает или задает полный адрес гиперссылки для фигуры.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_HRef()
```

## Примечания


Значение по умолчанию — пустая строка.

Ниже приведены примеры допустимых значений для этого свойства:

Полный URI: **https://www.aspose.com/**.

Полное имя файла: **C:\\My Documents\\SalesReport.doc**.

Относительный URI: **%../../../resource.txt**

Относительное имя файла: **%..\\My Documents\\SalesReport.doc**.

[Bookmark](../../../aspose.words/bookmark/) within another document: **https://www.aspose.com/Products/Default.aspx::Suites**

[Bookmark](../../../aspose.words/bookmark/) within this document: **%#BookmakName**.

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
