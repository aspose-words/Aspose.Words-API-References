---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto yöntemi"
linktitle: "get_MinorUnitIsAuto"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto yöntemi. C++'ta küçük işaretler arasındaki varsayılan mesafenin kullanılıp kullanılmayacağını belirten bir bayrağı alır veya ayarlar."
type: docs
weight: 18000
url: /tr/cpp/aspose.words.drawing.charts/chartaxis/get_minorunitisauto/
---
## ChartAxis::get_MinorUnitIsAuto method


Yardımcı işaret çizgileri arasındaki varsayılan mesafenin kullanılacağını gösteren bir bayrağı alır veya ayarlar.

```cpp
bool Aspose::Words::Drawing::Charts::ChartAxis::get_MinorUnitIsAuto()
```


## Örnekler



Bir grafik ekseninin işaretçilerini ve görüntülenen değerlerini nasıl manipüle edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(1, chart->get_Series()->get_Count());
ASSERT_EQ(u"Y-Values", chart->get_Series()->idx_get(0)->get_Name());

// Y-ekseninin küçük işaretçilerini çizim alanından dışarı doğru gösterecek şekilde ayarlayın,
// ve büyük işaretçileri ekseni kesecek şekilde ayarlayın.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisY();
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Outside);

// Y-eksenini her 10 birimde bir büyük işaretçi ve her 1 birimde bir küçük işaretçi gösterecek şekilde ayarlayın.
axis->set_MajorUnit(10);
axis->set_MinorUnit(1);

// Y-ekseninin sınırlarını -10 ve 20 olarak ayarlayın.
// Bu Y-ekseni artık 4 büyük işaretçi ve 27 küçük işaretçi gösterecek.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(20.0));

// X-ekseninde, büyük işaretçileri her 10 birimde bir ayarlayın,
// her küçük işaretçiyi 2.5 birimde bir ayarlayın.
axis = chart->get_AxisX();
axis->set_MajorUnit(10);
axis->set_MinorUnit(2.5);

// Her iki tür işaretçinin de grafik çizim alanının içinde görünmesini yapılandırın.
axis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
axis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);

// X-ekseninin sınırlarını, X-ekseninin 5 büyük işaretçi ve 12 küçük işaretçi kapsayacak şekilde ayarlayın.
axis->get_Scaling()->set_Minimum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(-10.0));
axis->get_Scaling()->set_Maximum(System::MakeObject<Aspose::Words::Drawing::Charts::AxisBound>(30.0));
axis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

ASSERT_EQ(1, axis->get_TickLabels()->get_Spacing());
ASPOSE_ASSERT_EQ(doc, axis->get_DisplayUnit()->get_Document());

// İşaretçi etiketlerini değerlerini milyonlar halinde gösterecek şekilde ayarlayın.
axis->get_DisplayUnit()->set_Unit(Aspose::Words::Drawing::Charts::AxisBuiltInUnit::Millions);

// İşaretçi etiketlerinin değerlerini göstereceği daha spesifik bir değeri ayarlayabiliriz.
// Bu ifade yukarıdakiyle eşdeğerdir.
axis->get_DisplayUnit()->set_CustomUnit(1000000);

doc->Save(get_ArtifactsDir() + u"Charts.AxisDisplayUnit.docx");
```

## Ayrıca Bakınız

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
