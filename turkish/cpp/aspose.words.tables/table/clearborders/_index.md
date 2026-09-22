---
title: "Aspose::Words::Tables::Table::ClearBorders yöntemi"
linktitle: "ClearBorders"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::ClearBorders yöntemi. Bu tabloda tüm tablo ve hücre kenarlıklarını kaldırır (C++)."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.tables/table/clearborders/
---
## Table::ClearBorders method


Bu tablodaki tüm tablo ve hücre kenarlıklarını kaldırır.

```cpp
void Aspose::Words::Tables::Table::ClearBorders()
```


## Örnekler



Bir tabloya dış kenarlık nasıl uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Tabloyu sayfanın ortasına hizalayın.
table->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);

// Tablodaki mevcut tüm kenarlıkları ve gölgelendirmeyi temizleyin.
table->ClearBorders();
table->ClearShading();

// Tablonun dış kenarına yeşil kenarlıklar ekleyin.
table->SetBorder(Aspose::Words::BorderType::Left, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Right, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);
table->SetBorder(Aspose::Words::BorderType::Bottom, Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green(), true);

// Hücreleri açık yeşil katı bir renk ile doldurun.
table->SetShading(Aspose::Words::TextureIndex::TextureSolid, System::Drawing::Color::get_LightGreen(), System::Drawing::Color::Empty);

doc->Save(get_ArtifactsDir() + u"Table.SetOutlineBorders.docx");
```


Bir tablodan tüm kenarlıkların nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Hello world!");
builder->EndTable();

// Üst kenarlığın rengini ve kalınlığını değiştirin.
System::SharedPtr<Aspose::Words::Border> topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
table->SetBorder(Aspose::Words::BorderType::Top, Aspose::Words::LineStyle::Double, 1.5, System::Drawing::Color::get_Red(), true);

ASPOSE_ASSERT_EQ(1.5, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Double, topBorder->get_LineStyle());

// Tablodaki tüm hücrelerin kenarlıklarını temizleyin ve ardından belgeyi kaydedin.
table->ClearBorders();
doc->Save(get_ArtifactsDir() + u"Table.ClearBorders.docx");

// Belgeyi yeniden açtıktan sonra tablonun özellik değerlerini doğrulayın.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Table.ClearBorders.docx");
table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
topBorder = table->get_FirstRow()->get_RowFormat()->get_Borders()->idx_get(Aspose::Words::BorderType::Top);

ASPOSE_ASSERT_EQ(0.0, topBorder->get_LineWidth());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), topBorder->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::None, topBorder->get_LineStyle());
```

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
