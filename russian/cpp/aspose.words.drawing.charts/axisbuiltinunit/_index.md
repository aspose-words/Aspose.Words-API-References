---
title: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit enum"
linktitle: "AxisBuiltInUnit"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::AxisBuiltInUnit enum. Указывает единицы отображения для оси в C++."
type: docs
weight: 20000
url: /ru/cpp/aspose.words.drawing.charts/axisbuiltinunit/
---
## AxisBuiltInUnit enum


Указывает единицы отображения для оси.

```cpp
enum class AxisBuiltInUnit
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Указывает, что значения на диаграмме отображаются как есть. |
| Пользовательский | 1 | Указывает, что значения на диаграмме должны делиться на пользовательский делитель. Это значение не поддерживается новыми типами диаграмм MS Office 2016. |
| Миллиарды | 2 | Указывает, что значения на диаграмме должны делиться на 1 000 000 000. |
| HundredMillions | 3 | Указывает, что значения на диаграмме должны делиться на 100 000 000. |
| Сотни | 4 | Указывает, что значения на диаграмме должны делиться на 100. |
| HundredThousands | 5 | Указывает, что значения на диаграмме должны быть разделены на 100 000. |
| Millions | 6 | Указывает, что значения на диаграмме должны быть разделены на 1 000 000. |
| TenMillions | 7 | Указывает, что значения на диаграмме должны быть разделены на 10 000 000. |
| TenThousands | 8 | Указывает, что значения на диаграмме должны быть разделены на 10 000. |
| Thousands | 9 | Указывает, что значения на диаграмме должны быть разделены на 1 000. |
| Trillions | 10 | Указывает, что значения на диаграмме должны быть разделены на 1 000 000 000 0000. |
| Percentage | 11 | Указывает, что значения на диаграмме должны быть разделены на 0,01. Это значение поддерживается только новыми типами диаграмм в MS Office 2016. |


## Примеры



Показывает, как управлять делениями и отображаемыми значениями оси диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Установите мелкие деления оси Y, направленные от области построения,
// а крупные деления — пересекать ось.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// Установите ось Y так, чтобы крупное деление отображалось каждые 10 единиц, а мелкое — каждые 1 единицу.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Установите границы оси Y на -10 и 20.
// Эта ось Y теперь будет отображать 4 крупные деления и 27 мелких делений.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// Для оси X установите крупные деления каждые 10 единиц,
// каждое мелкое деление — каждые 2,5 единицы.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Настройте оба типа делений так, чтобы они отображались внутри области построения графика.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// Установите границы оси X так, чтобы ось X охватывала 5 крупных делений и 12 мелких делений.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// Установите подписи делений отображать их значение в миллионах.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// Мы можем задать более конкретное значение, по которому подписи делений будут отображать свои значения.
// Это утверждение эквивалентно приведенному выше.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
