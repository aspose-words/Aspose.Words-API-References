---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge yöntemi"
linktitle: "get_VerticalMerge"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge yöntemi. C++'da hücrenin diğer hücrelerle dikey olarak nasıl birleştirileceğini belirtir."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


Hücrenin diğer hücrelerle dikey olarak nasıl birleştirildiğini belirtir.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## Açıklamalar


Hücreler yalnızca sol ve sağ sınırları aynıysa dikey olarak birleştirilebilir.

Hücreler dikey olarak birleştirildiğinde, birleştirilen hücrelerin görüntü alanları birleştirilir. Birleştirilmiş alan, ilk dikey birleştirilen hücrenin içeriğini göstermek için kullanılır ve diğer tüm dikey birleştirilen hücreler boş olmalıdır.

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

## Ayrıca Bakınız

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
