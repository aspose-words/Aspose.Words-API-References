---
title: "Aspose::Words::Drawing::Charts::IChartDataPoint интерфейс"
linktitle: "IChartDataPoint"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::IChartDataPoint интерфейс. Содержит свойства отдельной точки данных на диаграмме в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface


Содержит свойства отдельной точки данных на диаграмме.

```cpp
class IChartDataPoint : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [get_Bubble3D](./get_bubble3d/)() | Указывает, должны ли пузыри в диаграмме Bubble иметь применённый 3‑D эффект. |
| virtual [get_Explosion](./get_explosion/)() | Указывает величину, на которую точка данных должна быть смещена от центра круговой диаграммы. Может быть отрицательной; отрицательное значение означает, что свойство не установлено и взрыв не применяется. Применяется только к круговым диаграммам. |
| virtual [get_InvertIfNegative](./get_invertifnegative/)() | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| virtual [get_Marker](./get_marker/)() | Указывает маркер данных. Маркер автоматически создаётся по запросу. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Bubble3D](./set_bubble3d/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Bubble3D](./get_bubble3d/). |
| virtual [set_Explosion](./set_explosion/)(int32_t) | Сеттер для [Aspose::Words::Drawing::Charts::IChartDataPoint::get_Explosion](./get_explosion/). |
| virtual [set_InvertIfNegative](./set_invertifnegative/)(bool) | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
