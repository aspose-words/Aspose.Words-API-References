---
title: "Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment yöntemi"
linktitle: "get_RelativeHorizontalAlignment"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment yöntemi. Yüzen tablonun göreli yatay hizalamasını alır veya ayarlar C++'ta."
type: docs
weight: 30000
url: /tr/cpp/aspose.words.tables/table/get_relativehorizontalalignment/
---
## Table::get_RelativeHorizontalAlignment method


Yüzen tablonun göreceli yatay hizalamasını alır veya ayarlar.

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Tables::Table::get_RelativeHorizontalAlignment()
```


## Örnekler



Yüzen tabloların konumunun nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Tablonun konumunu sayfada bir yere ayarlayın, örneğin bu durumda sağ alt köşe.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Tabloyu eklediğimiz paragrafın konumundan puan cinsinden yatay ve dikey bir kaydırma da ayarlayabiliriz.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## Ayrıca Bakınız

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
