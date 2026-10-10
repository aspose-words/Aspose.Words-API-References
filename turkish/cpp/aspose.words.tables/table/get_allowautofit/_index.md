---
title: "Aspose::Words::Tables::Table::get_AllowAutoFit yöntemi"
linktitle: "get_AllowAutoFit"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_AllowAutoFit yöntemi. C++'da Microsoft Word ve Aspose.Words'in bir tablodaki hücreleri içeriklerine sığacak şekilde otomatik olarak yeniden boyutlandırmasını sağlar."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.tables/table/get_allowautofit/
---
## Table::get_AllowAutoFit method


Microsoft Word ve Aspose.Words'in bir tablodaki hücreleri içeriklerine sığacak şekilde otomatik olarak yeniden boyutlandırmasına izin verir.

```cpp
bool Aspose::Words::Tables::Table::get_AllowAutoFit()
```

## Açıklamalar


Varsayılan değer **true**'dır.

## Örnekler



Otomatik tablo hücresi yeniden boyutlandırmanın nasıl etkinleştirileceği/devre dışı bırakılacağı gösterilir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(100));
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder->EndRow();
builder->EndTable();

// Tablonun boyutlarını koruması için "AllowAutoFit" özelliğini "false" olarak ayarlayın
// tüm satır ve hücrelerinin boyutlarını korur ve içerikler sığamayacak kadar büyük olduğunda kırpar.
// Tablonun hücre genişliği ve yüksekliğini değiştirebilmesi için "AllowAutoFit" özelliğini "true" olarak ayarlayın.
// içeriklerine uyacak şekilde.
table->set_AllowAutoFit(allowAutoFit);

doc->Save(get_ArtifactsDir() + u"Table.AllowAutoFitOnTable.html");
```

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
