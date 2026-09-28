---
title: "Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode метод"
linktitle: "get_FormatCode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode метод. Получает или задает код формата, применяемый к значениям X в C++."
type: docs
weight: 2500
url: /ru/cpp/aspose.words.drawing.charts/chartxvaluecollection/get_formatcode/
---
## ChartXValueCollection::get_FormatCode method


Получает или задает код формата, применяемый к значениям X.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartXValueCollection::get_FormatCode()
```

## Примечания


Форматирование чисел используется для изменения отображения значений в диаграмме. Примеры числовых форматов:

Число - "#,##0.00"

Валюта - "\"\$\\"#,##0.00"

Время - "[$-x-systime]h:mm:ss AM/PM"

Дата - "d/mm/yyyy"

Процент - "0.00%"

Дробь - "# ?/?"

Экспоненциальный - "0.00E+00"

Бухгалтерский - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Пользовательский с цветом - "[Red]-#,##0.0"

## Примеры



Показывает, как работать с кодом формата данных диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте пузырьковую диаграмму.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Удалить автоматически сгенерированную серию.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// Показать метки данных.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// Установите коды формата данных.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## См. также

* Class [ChartXValueCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
