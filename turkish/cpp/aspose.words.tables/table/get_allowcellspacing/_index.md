---
title: "Aspose::Words::Tables::Table::get_AllowCellSpacing metodu"
linktitle: "get_AllowCellSpacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_AllowCellSpacing metodu. C++'ta \"Allow spacing between cells\" seçeneğini alır veya ayarlar."
type: docs
weight: 13000
url: /tr/cpp/aspose.words.tables/table/get_allowcellspacing/
---
## Table::get_AllowCellSpacing method


“Hücreler arasında boşluk bırakılmasına izin ver” seçeneğini alır veya ayarlar.

```cpp
bool Aspose::Words::Tables::Table::get_AllowCellSpacing()
```


## Örnekler



Bir tabloda bireysel hücreler arasındaki boşluğu nasıl etkinleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// Hücreler arasındaki boşluğu etkinleştirmek için "AllowCellSpacing" özelliğini "true" olarak ayarlayın
// "CellSpacing" özelliğinin değeri kadar bir büyüklükte, puan cinsinden.
// Hücre boşluğunu devre dışı bırakmak için "AllowCellSpacing" özelliğini "false" olarak ayarlayın
// ve "CellSpacing" özelliğinin değerini yok sayın.
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// "CellSpacing" özelliğini ayarlamak, hücre boşluğunu otomatik olarak etkinleştirir.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
