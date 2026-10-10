---
title: "Aspose::Words::Tables::Table::get_PreferredWidth yöntemi"
linktitle: "get_PreferredWidth"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_PreferredWidth yöntemi. Tablo tercih edilen genişliğini alır veya ayarlar C++'ta."
type: docs
weight: 29000
url: /tr/cpp/aspose.words.tables/table/get_preferredwidth/
---
## Table::get_PreferredWidth method


Tablonun tercih edilen genişliğini alır veya ayarlar.

```cpp
System::SharedPtr<Aspose::Words::Tables::PreferredWidth> Aspose::Words::Tables::Table::get_PreferredWidth()
```

## Açıklamalar


Varsayılan değer [Auto](../../preferredwidth/auto/)'dır.

## Örnekler



Bir tablonun sayfanın genişliğinin %50'sine otomatik olarak sığdırılmasını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```

## Ayrıca Bakınız

* Class [PreferredWidth](../../preferredwidth/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
