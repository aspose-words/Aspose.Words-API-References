---
title: "Aspose::Words::TextOrientation enum"
linktitle: "TextOrientation"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextOrientation enum. C++'da bir sayfadaki, tablo hücresindeki veya metin çerçevesindeki metnin yönünü belirtir."
type: docs
weight: 124000
url: /tr/cpp/aspose.words/textorientation/
---
## TextOrientation enum


Bir sayfadaki, tablo hücresindeki veya metin çerçevesindeki metnin yönünü belirtir.

```cpp
enum class TextOrientation
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Yatay | 0 | Metin yatay olarak düzenlenir (lr-tb). |
| Aşağı | 1 | Metin, üstten alta görünmesi için sağa doğru 90 derece döndürülür (tb-rl). |
| Yukarı | 3 | Metin, alttan üste görünmesi için sola doğru 90 derece döndürülür (bt-lr). |
| HorizontalRotatedFarEast | 4 | Metin yatay olarak düzenlenir, ancak Uzak Doğu karakterleri sola doğru 90 derece döndürülür (lr-tb-v). |
| VerticalFarEast | 5 | Uzak Doğu karakterleri dikey olarak görünür, diğer metin sağa doğru 90 derece döndürülerek üstten alta (tb-rl-v) görünür. |
| VerticalRotatedFarEast | 7 | Uzak Doğu karakterleri dikey olarak görünür, diğer metin sağa doğru 90 derece döndürülerek önce üstten alta dikey, ardından soldan sağa yatay (tb-lr-v) görünür. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
