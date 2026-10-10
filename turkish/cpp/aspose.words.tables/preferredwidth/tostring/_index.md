---
title: "Aspose::Words::Tables::PreferredWidth::ToString yöntemi"
linktitle: "ToString"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::PreferredWidth::ToString yöntemi. C++'de bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.tables/preferredwidth/tostring/
---
## PreferredWidth::ToString method


Bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür.

```cpp
System::String Aspose::Words::Tables::PreferredWidth::ToString() const override
```


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

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
