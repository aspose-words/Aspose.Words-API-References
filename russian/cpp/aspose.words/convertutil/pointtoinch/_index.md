---
title: "метод Aspose::Words::ConvertUtil::PointToInch"
linktitle: "PointToInch"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ConvertUtil::PointToInch. Преобразует пункты в дюймы в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil::PointToInch method


Преобразует пункты в дюймы.

```cpp
static double Aspose::Words::ConvertUtil::PointToInch(double points)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| пункты | double | Значение для преобразования. |

## Примеры



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

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
