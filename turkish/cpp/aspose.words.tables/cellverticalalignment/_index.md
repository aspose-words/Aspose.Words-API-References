---
title: "Aspose::Words::Tables::CellVerticalAlignment enum"
linktitle: "CellVerticalAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellVerticalAlignment enum. C++'da bir tablo hücresi içindeki metnin dikey hizalamasını belirtir."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.tables/cellverticalalignment/
---
## CellVerticalAlignment enum


Bir tablo hücresi içindeki metnin dikey hizalamasını belirtir.

```cpp
enum class CellVerticalAlignment
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Üst | 0 | Metin hücrenin üst kısmına hizalanır. |
| Orta | 1 | Metin hücrenin ortasına hizalanır. |
| Alt | 2 | Metin hücrenin alt kısmına hizalanır. |


## Örnekler



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
