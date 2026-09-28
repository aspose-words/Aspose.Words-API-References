---
title: "метод Aspose::Words::ConvertUtil::PixelToPoint"
linktitle: "PixelToPoint"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ConvertUtil::PixelToPoint. Преобразует пиксели в пункты при 96 dpi в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/convertutil/pixeltopoint/
---
## ConvertUtil::PixelToPoint(double) method


Преобразует пиксели в пункты при 96 dpi.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| пиксели | double | Значение для преобразования. |

## Примеры



Показывает, как задать свойства страницы в пикселях.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Раздела "Page Setup" определяет размер полей страницы в пунктах.
// Мы также можем использовать класс "ConvertUtil" для применения другой единицы измерения,
// например, пиксели при определении границ.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::PixelToPoint(125));

// Один пиксель равен 0,75 пункта.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToPixel(0.75));

// Используемое значение DPI по умолчанию — 96.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1, 96));

// Добавьте содержимое, чтобы продемонстрировать новые поля.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixels.docx");
```

## См. также

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## ConvertUtil::PixelToPoint(double, double) method


Преобразует пиксели в пункты при указанном разрешении пикселей.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels, double resolution)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| пиксели | double | Значение для преобразования. |
| разрешение | double | Разрешение dpi (точек на дюйм). |

## Примеры



Показывает, как использовать преобразование точек в пиксели с разрешением по умолчанию и пользовательским.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Определите размер верхнего поля этого раздела в пикселях, согласно пользовательскому DPI.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// При DPI по умолчанию 96 один пиксель равен 0,75 пункта.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Установите новое DPI и соответственно скорректируйте значение верхнего поля.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## См. также

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
