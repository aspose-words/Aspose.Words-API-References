---
title: "Aspose::Words::Tables::PreferredWidth::FromPoints yöntemi"
linktitle: "FromPoints"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::PreferredWidth::FromPoints yöntemi. C++'de bir dizi nokta kullanılarak belirtilen tercih edilen genişliği temsil eden yeni bir örnek döndüren bir oluşturma yöntemi."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth::FromPoints method


Puan sayısı kullanılarak belirtilen bir tercih edilen genişliği temsil eden yeni bir örnek döndüren bir oluşturma yöntemi.

```cpp
static System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::PreferredWidth::FromPoints(double points)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| puanlar | double | Değer 0 ile 22 inç arasında olmalıdır (22 * 72 nokta). |

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


Bir hücre için tercih edilen genişliği belirtirken birim dönüşüm araçlarının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(Aspose::Words::ConvertUtil::InchToPoint(3)));
builder->InsertCell();

ASPOSE_ASSERT_EQ(216.0, table->get_FirstRow()->get_FirstCell()->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Ayrıca Bakınız

* Class [PreferredWidth](../)
* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
