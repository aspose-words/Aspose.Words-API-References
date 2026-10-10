---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class. C++'da bir grafik serisi için baloncuk boyutlarının bir koleksiyonunu temsil eder."
type: docs
weight: 3500
url: /tr/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


Bir grafik serisi için balon boyutlarının bir koleksiyonunu temsil eder.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Count](./get_count/)() | Bu koleksiyondaki öğe sayısını alır. |
| [get_FormatCode](./get_formatcode/)() | Baloncuk boyutlarına uygulanan format kodunu alır veya ayarlar. |
| [GetEnumerator](./getenumerator/)() override | Bir enumeratör nesnesi döndürür. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Belirtilen indeksteki baloncuk boyutu değerini alır veya ayarlar. |
| [idx_set](./idx_set/)(int32_t, double) | Belirtilen indeksteki baloncuk boyutu değerini alır veya ayarlar. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/) için ayarlayıcı. |
| static [Type](./type/)() |  |
## Açıklamalar


Koleksiyon yalnızca balon boyutlarını değiştirmeye izin verir. Bir grafik serisine yeni değerler eklemek veya eklemek ya da değerleri kaldırmak için, uygun yöntemler [ChartSeries](../chartseries/) sınıfının kullanılabilir.

Boş balon boyutu değerleri **NaN** olarak temsil edilir.

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
