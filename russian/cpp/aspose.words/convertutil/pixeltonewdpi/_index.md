---
title: "метод Aspose::Words::ConvertUtil::PixelToNewDpi"
linktitle: "PixelToNewDpi"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ConvertUtil::PixelToNewDpi. Преобразует пиксели из одного разрешения в другое в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


Преобразует пиксели из одного разрешения в другое.

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| пиксели | double | Значение для преобразования. |
| oldDpi | double | Текущее разрешение dpi (точек на дюйм). |
| newDpi | double | Новое разрешение dpi (точек на дюйм). |

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
