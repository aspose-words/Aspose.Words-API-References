---
title: "Aspose::Words::Tables::Table::get_StyleOptions method"
linktitle: "get_StyleOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_StyleOptions yöntemi. C++'da bir tablo stilinin bu tabloya nasıl uygulandığını belirten bit bayraklarını alır veya ayarlar."
type: docs
weight: 37000
url: /tr/cpp/aspose.words.tables/table/get_styleoptions/
---
## Table::get_StyleOptions method


Bir tablo stilinin bu tabloya nasıl uygulandığını belirten bit bayraklarını alır veya ayarlar.

```cpp
Aspose::Words::Tables::TableStyleOptions Aspose::Words::Tables::Table::get_StyleOptions()
```


## Örnekler



Bir stil uygularken yeni bir tablo nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Herhangi bir tablo biçimlendirmesi ayarlamadan önce en az bir satır eklemeliyiz.
builder->InsertCell();

// Stil tanımlayıcısına göre kullanılan tablo stilini ayarlayın.
// .doc formatında kaydederken tüm tablo stillerinin mevcut olmadığını unutmayın.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Stili, tablo özelliklerine koşullara göre kısmen uygulayın, ardından tabloyu oluşturun.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## Ayrıca Bakınız

* Enum [TableStyleOptions](../../tablestyleoptions/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
