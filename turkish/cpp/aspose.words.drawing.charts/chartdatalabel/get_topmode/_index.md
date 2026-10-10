---
title: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode method"
linktitle: "get_TopMode"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode method. Top özelliği değerinin yorumlama modunu alır veya ayarlar: veri etiketinin konumunu grafiğin üst kenarından mı yoksa Position özelliğiyle belirtilen konumdan mı ayarladığını C++'ta."
type: docs
weight: 16667
url: /tr/cpp/aspose.words.drawing.charts/chartdatalabel/get_topmode/
---
## ChartDataLabel::get_TopMode method


Top özelliği değerinin yorumlama modunu alır veya ayarlar: veri etiketinin konumunu grafiğin üst kenarından mı yoksa [Position](../get_position/) özelliğiyle belirtilen konumdan mı ayarladığını.

```cpp
Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode Aspose::Words::Drawing::Charts::ChartDataLabel::get_TopMode()
```


## Örnekler



Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Varsayılan oluşturulan seriyi sil.
seriesColl->Clear();

// Lejantı gizle.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// Veri oluştur.
const int32_t dataLength = 20;
double totalValue = 0;
auto categories = System::MakeArray<System::String>(dataLength);
auto values = System::MakeArray<double>(dataLength, 0);

for (int32_t i = 0; i < dataLength; i++)
{
    categories[i] = System::String::Format(u"Category {0}", i);
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", categories, values);
series->set_HasDataLabels(true);

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->set_ShowLeaderLines(true);

// Position özelliği doughnut grafiklerinde kullanılamaz. Veri etiketlerini Left ve Top kullanarak yerleştirelim
// doughnut grafiğinin dışındaki bir daire etrafındaki özellikler
// Orijin, grafiğin sol üst köşesindedir.

const double titleAreaHeight = 25.5;
// Bu, başlık metni ve yazı tipi kullanılarak hesaplanabilir.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// Bu, etiket yazı tipi kullanılarak hesaplanabilir.
const double oneCharLabelWidth = 12.75;
// Bu, her etiket için metni ve yazı tipi kullanılarak hesaplanabilir.
const double twoCharLabelWidth = 17.25;
// Bu, her etiket için metni ve yazı tipi kullanılarak hesaplanabilir.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Veri noktaları üstten başladığı için, Left ve Top özelliklerinde kullanılan X koordinatları
// veri etiketleri sağa, Y koordinatları aşağıya işaret eder, başlangıç açısı -PI/2'dir.
double totalAngle = -System::Math::PI / 2;
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel> previousLabel;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel> dataLabel = dataLabels->idx_get(i);

    double value = series->get_YValues()->idx_get(i)->get_DoubleValue();
    double labelWidth;
    if (value < 10)
    {
        labelWidth = oneCharLabelWidth;
    }
    else
    {
        labelWidth = twoCharLabelWidth;
    }
    double labelSegmentAngle = value / totalValue * 2 * System::Math::PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System::Math::Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System::Math::Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // Mevcut veri etiketi diğer etiketlerle çakışıyorsa, onu yatay olarak taşıyın.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // Üstte sağa, altta sola hareket ettirin.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System::Math::PI);
        int32_t factor;
        if (isOnTop)
        {
            factor = 1;
        }
        else
        {
            factor = -1;
        }

        labelLeft = previousLabel->get_Left() + labelWidth * factor + labelMargin;
    }

    dataLabel->set_Left(labelLeft);
    dataLabel->set_LeftMode(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode::Absolute);
    dataLabel->set_Top(labelTop);
    dataLabel->set_TopMode(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode::Absolute);

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChartLabelPosition.docx");
```

## Ayrıca Bakınız

* Enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
