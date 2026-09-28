---
title: "Метод Aspose::Words::PageSetup::get_PageWidth"
linktitle: "get_PageWidth"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PageSetup::get_PageWidth. Возвращает или задает ширину страницы в пунктах в C++."
type: docs
weight: 36000
url: /ru/cpp/aspose.words/pagesetup/get_pagewidth/
---
## PageSetup::get_PageWidth method


Возвращает или задает ширину страницы в пунктах.

```cpp
double Aspose::Words::PageSetup::get_PageWidth()
```


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


Показывает, как вставить плавающее изображение и указать его позицию и размер.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Настройте свойство формы "RelativeHorizontalPosition", чтобы рассматривать значение свойства "Left"
// как горизонтальное расстояние формы в пунктах от левой стороны страницы.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);

// Установите горизонтальное расстояние формы от левой стороны страницы в 100.
shape->set_Left(100);

// Используйте свойство "RelativeVerticalPosition" аналогичным образом, чтобы разместить форму на 80 пунктов ниже верхней части страницы.
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Top(80);

// Установите высоту формы, при этом ширина будет автоматически масштабироваться для сохранения пропорций.
shape->set_Height(125);

ASPOSE_ASSERT_EQ(125.0, shape->get_Width());

// Свойства "Bottom" и "Right" содержат нижнюю и правую границы изображения.
ASPOSE_ASSERT_EQ(shape->get_Top() + shape->get_Height(), shape->get_Bottom());
ASPOSE_ASSERT_EQ(shape->get_Left() + shape->get_Width(), shape->get_Right());

doc->Save(get_ArtifactsDir() + u"Image.CreateFloatingPositionSize.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
