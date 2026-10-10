---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection class"
linktitle: "ChartSeriesGroupCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection sınıfı. C++'ta ChartSeriesGroup nesnelerinin bir koleksiyonunu temsil eder."
type: docs
weight: 17667
url: /tr/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class


Bir [ChartSeriesGroup](../chartseriesgroup/) nesnelerinin koleksiyonunu temsil eder.

```cpp
class ChartSeriesGroupCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [Add](./add/)(Aspose::Words::Drawing::Charts::ChartSeriesType) | Bu koleksiyona belirtilen seri tipinde yeni bir seri grubu ekler. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Bu koleksiyondaki seri gruplarının sayısını döndürür. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki bir [ChartSeriesGroup](../chartseriesgroup/) döndürür. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Belirtilen indeksteki bir seri grubunu kaldırır. Tüm alt seriler grafikten kaldırılacaktır. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Açıklama |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

## Örnekler



Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Varsayılan oluşturulan seriyi sil.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Ayrıca çizgi tipi bir ek seri grubu oluşturun.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Yeni seri grubu için ikincil eksenlerin kullanımını belirtin.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// İkincil X eksenini gizle.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// İkincil Y ekseninin başlığını tanımla.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Yeni seri grubuna bir seri ekle.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
