---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt metodu"
linktitle: "get_CrossesAt"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt yöntemi. C++'ta eksenin dikey eksen üzerinde nerede kesiştiğini belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.drawing.charts/chartaxis/get_crossesat/
---
## ChartAxis::get_CrossesAt method


Eksenin dik eksen üzerinde nerede kesildiğini belirtir.

```cpp
double Aspose::Words::Drawing::Charts::ChartAxis::get_CrossesAt()
```

## Açıklamalar


Bu özellik yalnızca [Crosses](../get_crosses/) [Custom](../../axiscrosses/) olarak ayarlandığında etkili olur. MS Office 2016 yeni grafikler tarafından desteklenmez.

Birimler eksenin türüne göre belirlenir. Eksen bir değer ekseni olduğunda, özelliğin değeri değer ekseninde ondalık bir sayıdır. Eksen bir zaman kategori ekseni olduğunda, değer temel tarihe (30/12/1899) göre gün sayısı olarak tanımlanır. Metin kategori ekseni için, değer ilk kategori olarak 1'den başlayan bir tam sayı kategori numarasıdır.

## Örnekler



Bir grafik ekseninin özel bir konumda kesilmesini nasıl yapacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Sütun grafiklerinde, Y ekseni varsayılan olarak sıfırda kesilir,
// bu, sıfırın altındaki tüm değerler için sütunların aşağı doğru işaret ederek negatif değerleri temsil ettiği anlamına gelir.
// Y ekseninin kesişme değerini farklı bir değere ayarlayabiliriz. Bu durumda, değeri 3 olarak ayarlayacağız.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> axis = chart->get_AxisX();
axis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Custom);
axis->set_CrossesAt(3);
axis->set_AxisBetweenCategories(true);

doc->Save(get_ArtifactsDir() + u"Charts.AxisCross.docx");
```

## Ayrıca Bakınız

* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
