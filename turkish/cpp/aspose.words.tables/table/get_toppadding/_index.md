---
title: "Aspose::Words::Tables::Table::get_TopPadding yöntemi"
linktitle: "get_TopPadding"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_TopPadding yöntemi. Hücre içeriklerinin üstüne eklenmesi gereken boşluk miktarını (puan cinsinden) alır veya ayarlar C++'da."
type: docs
weight: 40000
url: /tr/cpp/aspose.words.tables/table/get_toppadding/
---
## Table::get_TopPadding method


Hücre içeriklerinin üstüne eklenecek boşluk miktarını (puan cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::Tables::Table::get_TopPadding()
```


## Örnekler



Bir tabloda içerik doldurmasını nasıl yapılandıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// Tablodaki her hücre için, içeriği ile kenarları arasındaki mesafeyi ayarlayın.
// Bu tablo, metni kaydırarak minimum doldurma mesafesini koruyacaktır.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
