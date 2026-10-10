---
title: "Aspose::Words::DocumentBuilder::InsertChart yöntemi"
linktitle: "InsertChart"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertChart yöntemi. Bir grafik nesnesini belgeye ekler ve C++'ta belirtilen boyuta ölçeklendirir."
type: docs
weight: 30000
url: /tr/cpp/aspose.words/documentbuilder/insertchart/
---
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Belgeye eklenecek grafik türü. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Görüntüye olan mesafenin ölçüldüğü yeri belirtir. |
| left | double | Köken noktasından görüntünün sol tarafına kadar olan mesafe puan cinsinden. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Görüntüye olan mesafenin ölçüldüğü yeri belirtir. |
| üst | double | Köken noktasından görüntünün üst tarafına kadar olan mesafe puan cinsinden. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| wrapType | Aspose::Words::Drawing::WrapType | Metnin görüntünün etrafında nasıl sarılacağını belirtir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir grafik eklerken konum ve kaydırma nasıl belirtilir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::Margin, 100, 200, 100, Aspose::Words::Drawing::WrapType::Square);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertedChartRelativePosition.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType, Aspose::Words::Drawing::Charts::ChartStyle) method


Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Belgeye eklenecek grafik türü. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Görüntüye olan mesafenin ölçüldüğü yeri belirtir. |
| left | double | Köken noktasından görüntünün sol tarafına kadar olan mesafe puan cinsinden. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Görüntüye olan mesafenin ölçüldüğü yeri belirtir. |
| üst | double | Köken noktasından görüntünün üst tarafına kadar olan mesafe puan cinsinden. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| wrapType | Aspose::Words::Drawing::WrapType | Metnin görüntünün etrafında nasıl sarılacağını belirtir. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Eklenen grafiğin stili. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Ayrıca Bakınız

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


Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Belgeye eklenecek grafik türü. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Örnekler



Bir belgeye pasta grafiği nasıl eklenir gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, Aspose::Words::ConvertUtil::PixelToPoint(300), Aspose::Words::ConvertUtil::PixelToPoint(300))->get_Chart();
chart->get_Series()->Clear();
chart->get_Series()->Add(u"My fruit", System::MakeArray<System::String>({u"Apples", u"Bananas", u"Cherries"}), System::MakeArray<double>({1.3, 2.2, 1.5}));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertPieChart.docx");
```

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType, double, double, Aspose::Words::Drawing::Charts::ChartStyle) method


Belgeye bir grafik nesnesi ekler ve belirtilen boyuta ölçeklendirir.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertChart(Aspose::Words::Drawing::Charts::ChartType chartType, double width, double height, Aspose::Words::Drawing::Charts::ChartStyle chartStyle)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartType | Aspose::Words::Drawing::Charts::ChartType | Belgeye eklenecek grafik türü. |
| genişlik | double | Görüntünün genişliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| yükseklik | double | Görüntünün yüksekliği puan cinsinden. %100 ölçek talep etmek için negatif veya sıfır değer olabilir. |
| chartStyle | Aspose::Words::Drawing::Charts::ChartStyle | Eklenen grafiğin stili. |

### ReturnValue

Az önce eklenen görüntü düğümü.
## Açıklamalar


Bu metodun döndürdüğü [Shape](../../../aspose.words.drawing/shape/) nesnesini kullanarak görüntü boyutunu, konumunu, konumlandırma yöntemini ve diğer ayarları değiştirebilirsiniz.

## Ayrıca Bakınız

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [ChartType](../../../aspose.words.drawing.charts/charttype/)
* Enum [ChartStyle](../../../aspose.words.drawing.charts/chartstyle/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
