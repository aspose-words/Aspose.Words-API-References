---
title: "Перечисление Aspose::Words::Drawing::WrapType"
linktitle: "WrapType"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Drawing::WrapType. Указывает, как текст обтекает форму или изображение в C++."
type: docs
weight: 45000
url: /ru/cpp/aspose.words.drawing/wraptype/
---
## WrapType enum


Указывает, как текст обтекает фигуру или изображение.

```cpp
enum class WrapType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 3 | Текст не обтекает форму. Форма размещается позади или перед текстом. |
| Встроенный | 0 | Форма остаётся на том же слое, что и текст, и рассматривается как символ. |
| TopBottom | 1 | Текст останавливается в верхней части формы и продолжается на строке под формой. |
| Square | 2 | Обтекает текст вокруг всех сторон квадратного ограничивающего прямоугольника формы. |
| Tight | 4 | Плотно обтекает края формы, вместо обтекания ограничивающего прямоугольника. |
| Through | 5 | То же, что и Tight, но обтекает внутри открытых частей формы. |


## Примеры



Показывает, как вставить изображение и использовать его в качестве водяного знака.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте изображение в верхний колонтитул, чтобы оно было видно на каждой странице.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Разместите изображение в центре страницы.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```


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
