---
title: "Перечисление Aspose::Words::Drawing::RelativeVerticalPosition"
linktitle: "RelativeVerticalPosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::Drawing::RelativeVerticalPosition. Указывает, к чему относится вертикальное положение фигуры или текстового фрейма в C++."
type: docs
weight: 34000
url: /ru/cpp/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enum


Указывает, относительно чего определяется вертикальное положение фигуры или текстового фрейма.

```cpp
enum class RelativeVerticalPosition
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Поле | 0 | Указывает, что вертикальное позиционирование должно быть относительно полей страницы. |
| Page | 1 | Объект позиционируется относительно верхнего края страницы. |
| Paragraph | 2 | Объект позиционируется относительно верхней части абзаца, содержащего якорь. |
| Линия | 3 | Не документировано. |
| TopMargin | 4 | Указывает, что вертикальное позиционирование должно быть относительно верхнего поля текущей страницы. |
| BottomMargin | 5 | Указывает, что вертикальное позиционирование должно быть относительно нижнего поля текущей страницы. |
| InsideMargin | 6 | Указывает, что вертикальное позиционирование должно быть относительно внутреннего поля текущей страницы. |
| OutsideMargin | 7 | Указывает, что вертикальное позиционирование должно быть относительно внешнего поля текущей страницы. |
| TableDefault | n/a | Значение по умолчанию — [Margin](./). |
| TextFrameDefault | n/a | Значение по умолчанию — [Paragraph](./). |


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
