---
title: "Aspose::Words::ConvertUtil::MillimeterToPoint метод"
linktitle: "MillimeterToPoint"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ConvertUtil::MillimeterToPoint метод. Преобразует миллиметры в пункты в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


Преобразует миллиметры в пункты.

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| миллиметры | double | Значение для преобразования. |

## Примеры



Показывает, как задать свойства страницы в миллиметрах.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Раздела "Page Setup" определяет размер полей страницы в пунктах.
// Мы также можем использовать класс "ConvertUtil" для применения более привычной единицы измерения,
// например, миллиметры при определении границ.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// Один сантиметр примерно равен 28,3 пункта.
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// Добавьте содержимое, чтобы продемонстрировать новые поля.
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## См. также

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
