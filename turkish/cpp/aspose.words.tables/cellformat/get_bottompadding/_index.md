---
title: "Aspose::Words::Tables::CellFormat::get_BottomPadding metodu"
linktitle: "get_BottomPadding"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellFormat::get_BottomPadding metodu. Hücre içeriğinin altına eklemek için boşluk miktarını (nokta cinsinden) döndürür veya ayarlar C++'da."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.tables/cellformat/get_bottompadding/
---
## CellFormat::get_BottomPadding method


Hücre içeriğinin altına eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::Tables::CellFormat::get_BottomPadding()
```


## Örnekler



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

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
