---
title: "Aspose::Words::Tables::CellMerge enum"
linktitle: "CellMerge"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellMerge enum. Bir tablo hücresinin C++'ta diğer hücrelerle nasıl birleştirildiğini belirtir."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


Bir tablodaki hücrenin diğer hücrelerle nasıl birleştirileceğini belirtir.

```cpp
enum class CellMerge
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Hücre birleştirilmemiştir. |
| İlk | 1 | Hücre, birleştirilmiş hücreler aralığındaki ilk hücredir. |
| Önceki | 2 | Hücre, önceki hücreyle yatay ya da dikey olarak birleştirilir. |


## Örnekler



Tablo hücrelerini dikey olarak nasıl birleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// İlk satırın ilk sütununa bir hücre ekleyin.
// Bu hücre, dikey olarak birleştirilmiş hücreler aralığının ilk hücresi olacaktır.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// İlk satırın ikinci sütununa bir hücre ekleyin, ardından satırı sonlandırın.
// Ayrıca, oluşturulan hücrelerde dikey birleştirmeyi devre dışı bırakmak için oluşturucuyu yapılandırın.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// İkinci satırın ilk sütununa bir hücre ekleyin.
// Metin içeriği eklemek yerine, bu hücreyi doğrudan üstte eklediğimiz ilk hücreyle birleştireceğiz.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// İkinci satırın ikinci sütununa başka bir bağımsız hücre ekleyin.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```


Tablo hücrelerini yatay olarak nasıl birleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// İlk satırın ilk sütununa bir hücre ekleyin.
// Bu hücre, yatay olarak birleştirilmiş hücreler aralığının ilk hücresi olacaktır.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// İlk satırın ikinci sütununa bir hücre ekleyin. Metin içeriği eklemek yerine,
// bu hücreyi doğrudan sol tarafta eklediğimiz ilk hücreyle birleştireceğiz.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// İkinci satıra iki ayrı birleştirilmemiş hücre daha ekleyin.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
