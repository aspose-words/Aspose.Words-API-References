---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Text metodu"
linktitle: "get_Text"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Text metodu. Grafik başlığının metnini alır veya ayarlar. Null veya boş bir değer belirtilirse, C++'de otomatik oluşturulan başlık gösterilir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.drawing.charts/charttitle/get_text/
---
## ChartTitle::get_Text method


Grafik başlığının metnini alır veya ayarlar. **null** veya boş bir değer belirtilirse, otomatik oluşturulan başlık gösterilir.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartTitle::get_Text()
```


## Örnekler



Bir çizelge eklemeyi ve başlık ayarlamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir belge oluşturucu ile bir çizelge şekli ekleyin ve onun çizelgesini alın.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// "Title" özelliğini kullanarak çizelgemize bir başlık verin; bu başlık, çizelge alanının üst orta kısmında görünür.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// "Show" özelliğini "true" olarak ayarlayın, böylece başlık görünür olur.
title->set_Show(true);

// "Overlay" özelliğini "true" olarak ayarlayın Başlığa üst üste gelmelerine izin vererek diğer çizelge öğelerine daha fazla alan tanıyın.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Ayrıca Bakınız

* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
