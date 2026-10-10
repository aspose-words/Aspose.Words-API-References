---
title: "Aspose::Words::Tables::AutoFitBehavior enum"
linktitle: "AutoFitBehavior"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::AutoFitBehavior enum. Aspose.Words'in tabloyu, C++'ta AutoFit() yöntemini çağırdığınızda nasıl yeniden boyutlandırdığını belirler."
type: docs
weight: 10000
url: /tr/cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


Aspose.Words'in tabloyu, [AutoFit()](../table/autofit/) yöntemini çağırdığınızda nasıl yeniden boyutlandırdığını belirler.

```cpp
enum class AutoFitBehavior
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| AutoFitToContents | 0 | Aspose.Words AutoFit seçeneğini etkinleştirir, tablodan ve tüm hücrelerden tercih edilen genişliği kaldırır ve ardından tablo düzenini günceller. Ortaya çıkan tabloda, hücre genişlikleri tablo içeriğine sığacak şekilde güncellenir. Muhtemelen tablo küçülecektir. |
| AutoFitToWindow | 1 | Bu değeri kullandığınızda, Aspose.Words AutoFit seçeneğini etkinleştirir, tablonun tercih edilen genişliğini %100 olarak ayarlar, tüm hücrelerden tercih edilen genişlikleri kaldırır ve ardından tablo düzenini günceller. Sonuç olarak, tablo mevcut tüm genişliği kaplar ve hücre genişlikleri tablo içeriğine sığacak şekilde güncellenir. |
| FixedColumnWidths | 2 | Aspose.Words AutoFit seçeneğini devre dışı bırakır ve tablodan tercih edilen genişliği kaldırır. Hücrelerin genişlikleri, [Width](../cellformat/get_width/) özellikleriyle belirtilen şekilde kalır. |


## Örnekler



Bir stil uygularken yeni bir tablo nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Herhangi bir tablo biçimlendirmesi ayarlamadan önce en az bir satır eklemeliyiz.
builder->InsertCell();

// Stil tanımlayıcısına göre kullanılan tablo stilini ayarlayın.
// .doc formatında kaydederken tüm tablo stillerinin mevcut olmadığını unutmayın.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Stili, tablo özelliklerine koşullara göre kısmen uygulayın, ardından tabloyu oluşturun.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```


Biçimlendirilmiş 2x2 tablo nasıl oluşturulur gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Tablo oluşturulurken, belge oluşturucu mevcut RowFormat/CellFormat özellik değerlerini uygular
// imlecin bulunduğu mevcut satır/hücreye ve oluşturduğu yeni satır/hücrelere.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Daha önce eklenen satır ve hücreler, oluşturucunun biçimlendirme değişikliklerinden geriye dönük olarak etkilenmez.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
