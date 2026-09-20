---
title: "Aspose::Words::Drawing::Charts::AxisBound класс"
linktitle: "AxisBound"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::AxisBound класс. Представляет минимальное или максимальное ограничение значений оси. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.drawing.charts/axisbound/
---
## AxisBound class


Представляет минимальную или максимальную границу значений оси. Чтобы узнать больше, посетите статью документации [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisBound : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [AxisBound](./axisbound/)() | Создаёт новый экземпляр, указывающий, что ограничение оси должно определяться автоматически приложением для обработки текста. |
| [AxisBound](./axisbound/)(double) | Создаёт ограничение оси, представленное числом. |
| [AxisBound](./axisbound/)(System::DateTime) | Создаёт ограничение оси, представленное значением даты и времени. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_IsAuto](./get_isauto/)() const | Возвращает флаг, указывающий, что ограничение оси должно определяться автоматически. |
| [get_Value](./get_value/)() const | Возвращает числовое значение ограничения оси. |
| [get_ValueAsDate](./get_valueasdate/)() | Возвращает значение ограничения оси, представленное датой и временем. |
| [GetHashCode](./gethashcode/)() const override | Служит хеш-функцией для этого типа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Возвращает удобочитаемую строку, отображающую значение этого объекта. |
| static [Type](./type/)() |  |
## Примечания


Ограничение может быть указано как числовое, дата‑время или специальное значение "auto".

Экземпляры этого класса неизменяемы.

## Примеры



Показывает, как вставить диаграмму с значениями даты/времени.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Очистите демонстрационную серию данных диаграммы, чтобы начать с чистой диаграммы.
chart->get_Series()->Clear();

// Добавьте пользовательскую серию, содержащую значения даты/времени для оси X и соответствующие десятичные значения для оси Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::DateTime>({System::DateTime(2017, 11, 6), System::DateTime(2017, 11, 9), System::DateTime(2017, 11, 15), System::DateTime(2017, 11, 21), System::DateTime(2017, 11, 25), System::DateTime(2017, 11, 29)}), System::MakeArray<double>({1.2, 0.3, 2.1, 2.9, 4.2, 5.3}));

// Установите нижнее и верхнее ограничения для оси X.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 11, 5).ToOADate()));
xAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(System::DateTime(2017, 12, 3)));

// Установите основные единицы оси X в одну неделю, а вспомогательные единицы — в один день.
xAxis->set_BaseTimeUnit(Aspose::Words::Drawing::Charts::AxisTimeUnit::Days);
xAxis->set_MajorUnit(7.0);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MinorUnit(1.0);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);
xAxis->set_HasMajorGridlines(true);
xAxis->set_HasMinorGridlines(true);

// Определите свойства оси Y для десятичных значений.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::High);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(50.0);
yAxis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Hundreds);
yAxis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(100.0));
yAxis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(700.0));
yAxis->set_HasMajorGridlines(true);
yAxis->set_HasMinorGridlines(true);

doc->Save(get_ArtifactsDir() + u"Charts.DateTimeValues.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
