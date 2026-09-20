---
title: "Aspose::Words::Drawing::Charts::ChartSeries class"
linktitle: "ChartSeries"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries class. Представляет свойства серии диаграммы. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Представляет свойства серии диаграммы. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Добавляет указанное значение X в серию диаграммы. Если серия поддерживает значения Y и размеры пузырей, они будут пустыми для значения X. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Добавляет указанные значения X и Y в серию диаграммы. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Добавляет указанные значение X, значение Y и размер пузыря в серию диаграммы. |
| [Clear](./clear/)() | Удаляет все данные из серии диаграммы. Формат всех отдельных точек данных и подписей данных очищается. |
| [ClearValues](./clearvalues/)() | Удаляет все данные из серии диаграммы, сохраняя формат точек данных и подписей данных. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Копирует формат точки данных по умолчанию из точки данных с указанным индексом. |
| [get_Bubble3D](./get_bubble3d/)() override | Указывает, должны ли пузыри в диаграмме Bubble иметь применённый 3‑D эффект. |
| [get_BubbleSizes](./get_bubblesizes/)() | Возвращает коллекцию размеров пузырей для этой серии диаграммы. |
| [get_DataLabels](./get_datalabels/)() | Указывает настройки подписей данных для всей серии. |
| [get_DataPoints](./get_datapoints/)() const | Возвращает коллекцию объектов форматирования для всех точек данных в этой серии. |
| [get_Explosion](./get_explosion/)() override | Указывает величину, на которую точка данных должна быть смещена от центра круговой диаграммы. Может быть отрицательной; отрицательное значение означает, что свойство не установлено и взрыв не применяется. Применяется только к круговым диаграммам. |
| [get_Format](./get_format/)() | Обеспечивает доступ к форматированию заливки и линий серии. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Получает или задает флаг, указывающий, отображаются ли подписи данных для серии. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| [get_LegendEntry](./get_legendentry/)() | Получает запись легенды для этой серии диаграммы. |
| [get_Marker](./get_marker/)() override | Указывает маркер данных. Маркер автоматически создаётся по запросу. |
| [get_Name](./get_name/)() | Получает имя серии; если имя не задано явно, оно генерируется с использованием индекса. По умолчанию возвращает Series плюс один, основанный на индексе. |
| [get_SeriesType](./get_seriestype/)() | Получает тип этой серии диаграммы. |
| [get_Smooth](./get_smooth/)() const | Позволяет указать, должна ли линия, соединяющая точки на диаграмме, быть сглажена с использованием сплайнов Катмулла-Рома. |
| [get_XValues](./get_xvalues/)() | Получает коллекцию значений X для этой серии диаграммы. |
| [get_YValues](./get_yvalues/)() | Получает коллекцию значений Y для этой серии диаграммы. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Вставляет указанное значение X в серию диаграммы в указанный индекс. Если серия поддерживает значения Y и размеры пузырей, они будут пустыми для значения X. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Вставляет указанные значения X и Y в серию диаграммы в указанный индекс. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Вставляет указанные значение X, значение Y и размер пузыря в серию диаграммы в указанный индекс. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Удаляет значение X, значение Y и размер пузыря (если поддерживается) из серии диаграммы в указанном индексе. Соответствующая точка данных и подпись данных также удаляются. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeries::get_Bubble3D](./get_bubble3d/). |
| [set_Explosion](./set_explosion/)(int32_t) override | Указывает величину, на которую точка данных должна быть смещена от центра круговой диаграммы. Может быть отрицательной; отрицательное значение означает, что свойство не установлено и взрыв не применяется. Применяется только к круговым диаграммам. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Сеттер для [Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels](./get_hasdatalabels/). |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Указывает, должен ли родительский элемент инвертировать свои цвета, если значение отрицательное. |
| [set_Name](./set_name/)(const System::String\&) | Устанавливает имя серии; если имя не задано явно, оно генерируется с использованием индекса. По умолчанию возвращает Series плюс один, основанный на индексе. |
| [set_Smooth](./set_smooth/)(bool) | Позволяет указать, должна ли линия, соединяющая точки на диаграмме, быть сглажена с использованием сплайнов Катмулла-Рома. |
| static [Type](./type/)() |  |
## См. также

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
