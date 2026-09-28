---
title: "Класс Aspose::Words::Drawing::Charts::ChartDataPoint"
linktitle: "ChartDataPoint"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Drawing::Charts::ChartDataPoint. Позволяет задавать форматирование отдельной точки данных на диаграмме. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Позволяет указать форматирование отдельной точки данных на диаграмме. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormat](./clearformat/)() | Очищает формат этой точки данных. Свойства устанавливаются в значения по умолчанию, определённые в родительском ряду. |
| [get_Bubble3D](./get_bubble3d/)() override | Указывает, должны ли пузыри в диаграмме Bubble иметь применённый 3‑D эффект. |
| [get_Explosion](./get_explosion/)() override | Указывает величину, на которую точка данных должна быть смещена от центра круговой диаграммы. Может быть отрицательной; отрицательное значение означает, что свойство не установлено и взрыв не применяется. Применяется только к круговым диаграммам. |
| [get_Format](./get_format/)() | Предоставляет доступ к заполнению и форматированию линий этой точки данных. |
| [get_Index](./get_index/)() | Индекс точки данных, к которой применяется форматирование этим объектом. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| [get_Marker](./get_marker/)() override | Указывает маркер данных диаграммы. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Указывает, должны ли пузыри в диаграмме Bubble иметь применённый 3‑D эффект. |
| [set_Explosion](./set_explosion/)(int32_t) override | Сеттер для [Aspose::Words::Drawing::Charts::ChartDataPoint::get_Explosion](./get_explosion/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| static [Type](./type/)() |  |
## См. также

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
