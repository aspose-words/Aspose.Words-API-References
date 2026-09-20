---
title: "Aspose::Words::DocumentBuilder::InsertChart метод"
linktitle: "InsertChart"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::InsertChart. Вставляет объект диаграммы в документ и масштабирует его до указанного размера в C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Вставляет объект диаграммы в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Тип диаграммы, который будет вставлен в документ. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | double | Расстояние в пунктах от начала координат до левой стороны изображения. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Указывает, как обтекать текст вокруг изображения. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как указать позицию и обтекание при вставке диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


Вставляет объект диаграммы в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Тип диаграммы, который будет вставлен в документ. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Указывает, откуда измеряется расстояние до изображения. |
| left | double | Расстояние в пунктах от начала координат до левой стороны изображения. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Указывает, откуда измеряется расстояние до изображения. |
| top | double | Расстояние в пунктах от начала координат до верхней стороны изображения. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Указывает, как обтекать текст вокруг изображения. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Стиль вставленной диаграммы. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double) method


Вставляет объект диаграммы в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Тип диаграммы, который будет вставлен в документ. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## Примеры



Показывает, как вставить круговую диаграмму в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


Вставляет объект диаграммы в документ и масштабирует его до указанного размера.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Тип диаграммы, который будет вставлен в документ. |
| width | double | Ширина изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Стиль вставленной диаграммы. |

### ReturnValue

Узел изображения, который только что был вставлен.
## Примечания


Вы можете изменить размер изображения, его расположение, способ позиционирования и другие параметры, используя объект [Shape](../../../aspose.words.drawing/shape/), возвращаемый этим методом.

## См. также

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
