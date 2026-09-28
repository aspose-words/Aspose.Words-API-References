---
title: "Перечисление Aspose::Words::Drawing::HorizontalAlignment"
linktitle: "HorizontalAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Drawing::HorizontalAlignment. Указывает горизонтальное выравнивание плавающей фигуры, текстового фрейма или плавающей таблицы в C++."
type: docs
weight: 26000
url: /ru/cpp/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enum


Указывает горизонтальное выравнивание плавающей фигуры, текстовой рамки или плавающей таблицы.

```cpp
enum class HorizontalAlignment
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Объект явно позиционируется, обычно используя его свойство **Left**. |
| Default | n/a | То же, что и [None](./). |
| Слева | 1 | Указывает, что объект должен быть выровнен по левому краю относительно базового горизонтального выравнивания. |
| По центру | 2 | Указывает, что объект должен быть центрирован относительно базового горизонтального выравнивания. |
| Справа | 3 | Указывает, что объект должен быть выровнен по правому краю относительно базовой горизонтальной выравнивающей линии. |
| Внутри | 4 | Указывает, что объект должен находиться внутри базовой горизонтальной выравнивающей основы. |
| Снаружи | 5 | Указывает, что объект должен находиться за пределами базовой горизонтальной выравнивающей линии. |


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
