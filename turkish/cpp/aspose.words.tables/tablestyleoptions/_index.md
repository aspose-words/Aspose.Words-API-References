---
title: "Aspose::Words::Tables::TableStyleOptions enum"
linktitle: "TableStyleOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::TableStyleOptions enum. C++'ta bir tabloya tablo stilinin nasıl uygulandığını belirtir."
type: docs
weight: 15000
url: /tr/cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


Tablo stilinin bir tabloya nasıl uygulandığını belirtir.

```cpp
enum class TableStyleOptions
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 | Hiçbir tablo stili biçimlendirmesi uygulanmaz. |
| FirstRow | 32 | İlk satır koşullu biçimlendirmesini uygulayın. |
| LastRow | 64 | Son satır koşullu biçimlendirmesini uygulayın. |
| FirstColumn | 128 | İlk sütun için 1 koşullu biçimlendirme uygulayın. |
| LastColumn | 256 | Son sütun koşullu biçimlendirmesini uygulayın. |
| RowBands | 512 | Satır bantlaması koşullu biçimlendirmesini uygulayın. |
| ColumnBands | 1024 | Sütun bantlaması koşullu biçimlendirmesini uygulayın. |
| Default2003 | n/a | [Row](../row/) ve sütun bantlaması uygulanır. Bu, DOC, WML ve RTF gibi eski formatlar için Microsoft Word varsayılanıdır. |
| Default | n/a | Bu, Microsoft Word varsayılanlarıdır. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
