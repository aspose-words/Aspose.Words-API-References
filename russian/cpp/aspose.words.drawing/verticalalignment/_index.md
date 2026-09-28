---
title: "Aspose::Words::Drawing::VerticalAlignment enum"
linktitle: "VerticalAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::VerticalAlignment enum. Указывает вертикальное выравнивание плавающей формы, текстовой рамки или плавающей таблицы в C++."
type: docs
weight: 43000
url: /ru/cpp/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enum


Указывает вертикальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы.

```cpp
enum class VerticalAlignment
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Объект явно позиционируется, обычно используя его свойство **Top**. |
| Верх | 1 | Указывает, что объект должен находиться в верхней части базовой вертикальной выравнивающей основы. |
| По центру | 2 | Указывает, что объект должен быть центрирован относительно базовой вертикальной выравнивающей основы. |
| Низ | 3 | Указывает, что объект должен находиться в нижней части базовой вертикальной выравнивающей основы. |
| Внутри | 4 | Указывает, что объект должен находиться внутри базовой горизонтальной выравнивающей основы. |
| Снаружи | 5 | Указывает, что объект должен находиться за пределами базовой вертикальной выравнивающей основы. |
| Встроенный | -1 | Не документировано. Похоже, это возможное значение для плавающих абзацев и таблиц. |
| Default | n/a | То же, что и [None](./). |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
