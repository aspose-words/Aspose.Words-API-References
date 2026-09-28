---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel class"
linktitle: "ChartDataLabel"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel class. Представляет подпись данных на точке диаграммы или трендовой линии. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Представляет подпись данных на точке диаграммы или линии тренда. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormat](./clearformat/)() | Очищает формат этой подписи данных. Свойства устанавливаются в значения по умолчанию, определённые в родительской коллекции подписей данных. |
| [get_Font](./get_font/)() | Предоставляет доступ к форматированию шрифта этой подписи данных. |
| [get_Format](./get_format/)() | Предоставляет доступ к заполнению и форматированию линий подписи данных. |
| [get_Index](./get_index/)() | Указывает индекс содержащего элемента. Этот индекс определяет, к какой из коллекций дочерних элементов родителя применяется данный элемент. Значение по умолчанию — 0. |
| [get_IsHidden](./get_ishidden/)() | Получает/устанавливает флаг, указывающий, скрыта ли эта подпись. Значение по умолчанию — **false**. |
| [get_IsVisible](./get_isvisible/)() | Возвращает **true**, если у этой подписи данных есть что отображать. |
| [get_Left](./get_left/)() | Получает или устанавливает расстояние подписи данных в пунктах от левого края диаграммы или от позиции, указанной в её свойстве [Position](./get_position/), в зависимости от значения свойства [LeftMode](./get_leftmode/). |
| [get_LeftMode](./get_leftmode/)() | Получает или устанавливает режим интерпретации значения свойства [Left](./get_left/): определяет, задаёт ли он расположение подписи данных от левого края диаграммы или от позиции, указанной в её свойстве [Position](./get_position/). |
| [get_NumberFormat](./get_numberformat/)() | Возвращает числовой формат родительского элемента. |
| [get_Orientation](./get_orientation/)() | Получает или устанавливает ориентацию текста подписи. |
| [get_Position](./get_position/)() | Получает или устанавливает позицию подписи данных. |
| [get_Rotation](./get_rotation/)() | Получает или устанавливает вращение подписи в градусах. |
| [get_Separator](./get_separator/)() | Получает строковый разделитель, используемый для подписей данных на диаграмме. По умолчанию это запятая, за исключением круговых диаграмм, показывающих только название категории и процент, где вместо неё используется разрыв строки. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Позволяет указать, следует ли отображать размер пузыря для подписей данных на диаграмме. Применяется только к пузырьковым диаграммам. Значение по умолчанию — **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Позволяет указать, следует ли отображать название категории в подписи данных на диаграмме. Значение по умолчанию — **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Позволяет указать, следует ли отображать значения из диапазона подписи данных в подписи данных. Значение по умолчанию — **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Позволяет указать, следует ли показывать линии-выноски подписи данных. Значение по умолчанию — **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Позволяет указать, следует ли отображать ключ легенды в подписи данных на диаграмме. Значение по умолчанию — **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Позволяет указать, следует ли отображать процентное значение в подписи данных на диаграмме. Значение по умолчанию — **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Возвращает логическое значение, указывающее поведение отображения имени серии в подписи данных на диаграмме. **true** — показать имя серии; **false** — скрыть. По умолчанию **false**. |
| [get_ShowValue](./get_showvalue/)() | Позволяет указать, следует ли отображать значения в подписи данных. Значение по умолчанию — **false**. |
| [get_Top](./get_top/)() | Получает или задает расстояние подписи данных в пунктах от верхнего края диаграммы или от позиции, указанной её свойством [Position](./get_position/), в зависимости от значения свойства [TopMode](./get_topmode/). |
| [get_TopMode](./get_topmode/)() | Получает или задает режим интерпретации значения свойства [Top](./get_top/): задаёт ли он расположение подписи данных от верхнего края диаграммы или от позиции, указанной её свойством [Position](./get_position/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Получает/устанавливает флаг, указывающий, скрыта ли эта подпись. Значение по умолчанию — **false**. |
| [set_Left](./set_left/)(double) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Left](./get_left/). |
| [set_LeftMode](./set_leftmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode](./get_leftmode/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::ChartDataLabelPosition) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Rotation](./get_rotation/). |
| [set_Separator](./set_separator/)(const System::String\&) | Устанавливает разделитель строк, используемый в подписи данных на диаграмме. По умолчанию — запятая, за исключением круговых диаграмм, показывающих только название категории и процент, где вместо этого используется разрыв строки. |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Позволяет указать, следует ли отображать название категории в подписи данных на диаграмме. Значение по умолчанию — **false**. |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Позволяет указать, следует ли отображать значения из диапазона подписи данных в подписи данных. Значение по умолчанию — **false**. |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Позволяет указать, следует ли показывать линии-выноски подписи данных. Значение по умолчанию — **false**. |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Позволяет указать, следует ли отображать ключ легенды в подписи данных на диаграмме. Значение по умолчанию — **false**. |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Позволяет указать, следует ли отображать процентное значение в подписи данных на диаграмме. Значение по умолчанию — **false**. |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Устанавливает логическое значение, указывающее поведение отображения имени серии в подписи данных на диаграмме. **true** — показать имя серии; **false** — скрыть. По умолчанию **false**. |
| [set_ShowValue](./set_showvalue/)(bool) | Позволяет указать, следует ли отображать значения в подписи данных. Значение по умолчанию — **false**. |
| [set_Top](./set_top/)(double) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Top](./get_top/). |
| [set_TopMode](./set_topmode/)(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode) | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode](./get_topmode/). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
