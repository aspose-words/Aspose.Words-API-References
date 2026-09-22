---
title: "Aspose::Words::Tables::PreferredWidthType enum"
linktitle: "PreferredWidthType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::PreferredWidthType enum. C++'da bir tablo veya hücrenin tercih edilen genişliği için ölçü birimini belirtir."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Bir tablo veya hücrenin tercih edilen genişliği için ölçü birimini belirtir.

```cpp
enum class PreferredWidthType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Otomatik | 1 | Tercih edilen genişlik belirtilmemiştir. Tablo veya hücrenin gerçek genişliği ya açıkça belirtilen genişlik kullanılarak belirlenir ya da tablo görüntülendiğinde tablo yerleşim algoritması tarafından otomatik olarak belirlenir; bu, tablo otomatik sığdırma ayarına bağlıdır. |
| Yüzde | 2 | Belirtilen bir yüzde kullanarak mevcut öğe genişliğini ölç. |
| Puan | 3 | Belirtilen bir puan sayısı (1/72 inç) kullanarak mevcut öğe genişliğini ölç. |


## Örnekler



Bir tablo hücresinin tercih edilen genişlik türünü ve değerini nasıl doğrulayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
