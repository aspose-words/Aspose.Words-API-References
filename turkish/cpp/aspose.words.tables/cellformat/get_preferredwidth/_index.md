---
title: "Aspose::Words::Tables::CellFormat::get_PreferredWidth metodu"
linktitle: "get_PreferredWidth"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellFormat::get_PreferredWidth metodu. Hücrenin tercih edilen genişliğini C++'da döndürür veya ayarlar."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.tables/cellformat/get_preferredwidth/
---
## CellFormat::get_PreferredWidth method


Hücrenin tercih edilen genişliğini alır veya ayarlar.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::CellFormat::get_PreferredWidth()
```

## Açıklamalar


Tercih edilen genişlik (tablonun Otomatik Sığdırma seçeneğiyle birlikte) hücrenin gerçek genişliğinin tablo yerleşim algoritması tarafından nasıl hesaplandığını belirler. [Table](../../table/) yerleşimi, belgeyi kaydederken Aspose.Words tarafından veya belgeyi görüntülerken Microsoft Word tarafından gerçekleştirilebilir.

Tercih edilen genişlik nokta cinsinden veya yüzde olarak belirtilebilir. Tercih edilen genişlik ayrıca "auto" olarak da belirtilebilir, bu da hiçbir tercih edilen genişliğin belirtilmediği anlamına gelir.

Varsayılan değer [Auto](../../preferredwidth/auto/)'dır.

## Örnekler



Tablo hücreleri için tercih edilen bir genişliğin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// "PreferredWidth" sınıfını tablo hücrelerine uygulamanın iki yolu vardır.
// 1 -  Noktalara dayalı mutlak bir tercih edilen genişlik ayarlayın:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Tablo genişliğinin yüzdesine dayalı göreceli bir tercih edilen genişlik ayarlayın:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// Tercih edilen genişlik belirtilmemiş bir hücre, mevcut alanın geri kalanını kaplayacaktır.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// "PreferredWidth" özelliğinin her yapılandırması yeni bir nesne oluşturur.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## Ayrıca Bakınız

* Class [PreferredWidth](../../preferredwidth/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
