---
title: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge metodu"
linktitle: "get_HorizontalMerge"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge metodu. Hücrenin satırdaki diğer hücrelerle yatay olarak nasıl birleştirileceğini C++'da belirtir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


Hücrenin satırdaki diğer hücrelerle yatay olarak nasıl birleştirileceğini belirtir.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## Örnekler



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

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
