---
title: "Aspose::Words::HeightRule enum"
linktitle: "HeightRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::HeightRule enum. C++'da bir nesnenin yüksekliğini belirleme kuralını belirtir."
type: docs
weight: 91000
url: /tr/cpp/aspose.words/heightrule/
---
## HeightRule enum


Bir nesnenin yüksekliğini belirleme kuralını belirtir.

```cpp
enum class HeightRule
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| AtLeast | 0 | Yükseklik, belirtilen nokta cinsinden en az yüksekliğe sahip olacaktır. Gerekirse, nesne içindeki tüm metni sığdırmak için büyüyecektir. |
| Exactly | 1 | Yükseklik, nokta cinsinden tam olarak belirtilir. Lütfen, metin bu yüksekliğe sahip nesneye sığmazsa kesileceğini unutmayın. |
| Otomatik | 2 | Yükseklik, nesne içindeki tüm metni sığdırmak için otomatik olarak büyüyecektir. |


## Örnekler



Bir belge oluşturucu ile satırların nasıl biçimlendirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// İkinci bir satır başlatın ve ardından yüksekliğini yapılandırın. Oluşturucu bu ayarları şuraya uygulayacaktır
// mevcut satırına ve sonradan oluşturacağı yeni satırlara.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// İlk satır, dolgu yeniden yapılandırmasından etkilenmedi ve hâlâ varsayılan değerleri tutmaktadır.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
