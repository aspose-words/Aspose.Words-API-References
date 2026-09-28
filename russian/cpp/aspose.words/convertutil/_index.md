---
title: "Aspose::Words::ConvertUtil class"
linktitle: "ConvertUtil"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ConvertUtil class. Предоставляет вспомогательные функции для преобразования между различными единицами измерения. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words/convertutil/
---
## ConvertUtil class


Предоставляет вспомогательные функции для преобразования между различными единицами измерения. Чтобы узнать больше, посетите статью документации [Convert Between Measurement Units](https://docs.aspose.com/words/cpp/convert-between-measurement-units/).

```cpp
class ConvertUtil
```

## Методы

| Метод | Описание |
| --- | --- |
| [ConvertUtil](./convertutil/)() |  |
| static [InchToPoint](./inchtopoint/)(double) | Преобразует дюймы в пункты. |
| static [MillimeterToPoint](./millimetertopoint/)(double) | Преобразует миллиметры в пункты. |
| static [PixelToNewDpi](./pixeltonewdpi/)(double, double, double) | Преобразует пиксели из одного разрешения в другое. |
| static [PixelToPoint](./pixeltopoint/)(double) | Преобразует пиксели в пункты при 96 dpi. |
| static [PixelToPoint](./pixeltopoint/)(double, double) | Преобразует пиксели в пункты при указанном разрешении пикселей. |
| static [PointToInch](./pointtoinch/)(double) | Преобразует пункты в дюймы. |
| static [PointToPixel](./pointtopixel/)(double) | Преобразует пункты в пиксели при 96 dpi. |
| static [PointToPixel](./pointtopixel/)(double, double) | Преобразует пункты в пиксели при указанном разрешении пикселей. |

## Примеры



Показывает, как настроить размер бумаги, ориентацию, поля и другие параметры раздела.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


Показывает, как задать свойства страницы в дюймах.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Раздела "Page Setup" определяет размер полей страницы в пунктах.
// Мы также можем использовать класс "ConvertUtil" для применения более привычной единицы измерения,
// например, дюймы при определении границ.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// Один дюйм равен 72 пунктам.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// Добавьте содержимое, чтобы продемонстрировать новые поля.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
