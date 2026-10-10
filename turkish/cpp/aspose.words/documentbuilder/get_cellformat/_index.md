---
title: "Aspose::Words::DocumentBuilder::get_CellFormat yöntemi"
linktitle: "get_CellFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::get_CellFormat yöntemi. C++'ta mevcut tablo hücresi biçimlendirme özelliklerini temsil eden bir nesne döndürür."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/documentbuilder/get_cellformat/
---
## DocumentBuilder::get_CellFormat method


Geçerli tablo hücresi biçimlendirme özelliklerini temsil eden bir nesne döndürür.

```cpp
System::SharedPtr<Aspose::Words::Tables::CellFormat> Aspose::Words::DocumentBuilder::get_CellFormat()
```


## Örnekler



Özel kenarlıklarla bir tablo oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Bir DocumentBuilder için tablo biçimlendirme seçeneklerini ayarlama
// Bunları, onunla eklediğimiz her satır ve hücreye uygular.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Biçimlendirmeyi değiştirmek, mevcut hücreye uygulanır,
// ve ardından builder ile oluşturduğumuz yeni hücrelere de.
// Bu, daha önce eklediğimiz hücreleri etkilemez.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Dikey metni sığdırmak için satır yüksekliğini artırın.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
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


Bir belge oluşturucu ile hücrelerin nasıl biçimlendirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// İkinci bir hücre ekleyin ve ardından hücre metni doldurma seçeneklerini yapılandırın.
// Builder bu ayarları mevcut hücresine uygulayacak ve ardından oluşturulan yeni hücrelere de uygulayacaktır.
builder->InsertCell();

System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = builder->get_CellFormat();
cellFormat->set_Width(250);
cellFormat->set_LeftPadding(30);
cellFormat->set_RightPadding(30);
cellFormat->set_TopPadding(30);
cellFormat->set_BottomPadding(30);

builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->EndTable();

// İlk hücre, dolgu yeniden yapılandırmasından etkilenmedi ve hâlâ varsayılan değerleri tutuyor.
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(5.4, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(0.0, table->get_FirstRow()->get_Cells()->idx_get(0)->get_CellFormat()->get_BottomPadding());

ASPOSE_ASSERT_EQ(250.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_Width());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_LeftPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_RightPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_TopPadding());
ASPOSE_ASSERT_EQ(30.0, table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_BottomPadding());

// İlk hücre, çıktı belgesinde komşu hücrenin boyutuna eşit olacak şekilde büyümeye devam edecektir.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetCellFormatting.docx");
```

## Ayrıca Bakınız

* Class [CellFormat](../../../aspose.words.tables/cellformat/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
