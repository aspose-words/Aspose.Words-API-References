---
title: "Aspose::Words::TextColumnCollection::idx_get yöntemi"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TextColumnCollection::idx_get yöntemi. C++'ta belirtilen indeksteki bir metin sütununu döndürür."
type: docs
weight: 8000
url: /tr/cpp/aspose.words/textcolumncollection/idx_get/
---
## TextColumnCollection::idx_get method


Belirtilen indeksteki bir metin sütununu döndürür.

```cpp
System::SharedPtr<Aspose::Words::TextColumn> Aspose::Words::TextColumnCollection::idx_get(int32_t index)
```


## Örnekler



Düzensiz aralıklı sütunların nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Sütunları düzenlemek için mevcut olan alan miktarını belirleyin.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// İlk sütunu dar olarak ayarlayın.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// İkinci sütunu, sayfanın kenar boşlukları içinde mevcut olan kalan alanı alacak şekilde ayarlayın.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Ayrıca Bakınız

* Class [TextColumn](../../textcolumn/)
* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
