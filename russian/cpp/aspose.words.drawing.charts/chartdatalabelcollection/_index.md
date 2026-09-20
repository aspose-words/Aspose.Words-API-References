---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection класс"
linktitle: "ChartDataLabelCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Drawing::Charts::ChartDataLabelCollection. Представляет коллекцию ChartDataLabel. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class


Представляет коллекцию [ChartDataLabel](../chartdatalabel/). Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabelCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel>>,
                                 public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                                 public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormat](./clearformat/)() | Очищает формат всех [ChartDataLabel](../chartdatalabel/) в этой коллекции. |
| [get_Count](./get_count/)() | Возвращает количество [ChartDataLabel](../chartdatalabel/) в этой коллекции. |
| [get_Font](./get_font/)() | Предоставляет доступ к форматированию шрифта подписей данных всей серии. |
| [get_Format](./get_format/)() | Предоставляет доступ к заполнению и форматированию линий подписей данных. |
| [get_NumberFormat](./get_numberformat/)() | Получает экземпляр [ChartNumberFormat](../chartnumberformat/), позволяющий задать числовой формат для подписей данных всей серии. |
| [get_Orientation](./get_orientation/)() | Получает или задает ориентацию текста подписей данных всей серии. |
| [get_Position](./get_position/)() | Получает или задает позицию подписей данных. |
| [get_Rotation](./get_rotation/)() | Получает или задает вращение подписей данных всей серии в градусах. |
| [get_Separator](./get_separator/)() | Получает или задает строковый разделитель, используемый для подписей данных всей серии. По умолчанию — запятая, за исключением круговых диаграмм, показывающих только название категории и процент, где вместо этого используется разрыв строки. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Позволяет указать, следует ли отображать размер пузыря в подписях данных всей серии. Применяется только к пузырьковым диаграммам. Значение по умолчанию — **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Позволяет указать, следует ли отображать название категории в подписях данных всей серии. Значение по умолчанию — **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Позволяет указать, следует ли отображать значения из диапазона подписей данных в подписях всей серии. Значение по умолчанию — **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Позволяет указать, следует ли показывать линии‑выноски подписей данных всей серии. Значение по умолчанию — **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Позволяет указать, следует ли отображать ключ легенды в подписях данных всей серии. Значение по умолчанию — **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Позволяет указать, следует ли отображать процентное значение в подписях данных всей серии. Значение по умолчанию — **false**. Применяется только к круговым диаграммам. |
| [get_ShowSeriesName](./get_showseriesname/)() | Возвращает или задает логическое значение, указывающее поведение отображения названия серии в подписях данных всей серии. **true** — показывать название серии; **false** — скрывать. По умолчанию **false**. |
| [get_ShowValue](./get_showvalue/)() | Позволяет указать, следует ли отображать значения в подписях данных всей серии. Значение по умолчанию — **false**. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает [ChartDataLabel](../chartdatalabel/) для указанного индекса. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Позволяет указать, следует ли отображать значения из диапазона подписей данных в подписях всей серии. Значение по умолчанию — **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowValue](./get_showvalue/). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
