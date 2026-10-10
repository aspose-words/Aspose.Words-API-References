---
title: "Aspose::Words::Tables::Table::AutoFit yöntemi"
linktitle: "AutoFit"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::AutoFit yöntemi. C++'da belirtilen otomatik sığdırma davranışına göre tabloyu ve hücreleri yeniden boyutlandırır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.tables/table/autofit/
---
## Table::AutoFit method


Belirtilen otomatik sığdırma davranışına göre tabloyu ve hücreleri yeniden boyutlandırır.

```cpp
void Aspose::Words::Tables::Table::AutoFit(Aspose::Words::Tables::AutoFitBehavior behavior)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| davranış | Aspose::Words::Tables::AutoFitBehavior | Tablonun nasıl otomatik sığdırılacağını belirtir. |
## Açıklamalar


Bu yöntem, Microsoft Word'de bir tablo için Auto Fit menüsünde bulunan komutları taklit eder. Mevcut komutlar \"Auto Fit to Contents\", \"Auto Fit to Window\" ve \"Fixed Column Width\"'dır. Microsoft Word'de bu komutlar ilgili tablo özelliklerini ayarlar ve ardından tablo düzenini günceller; Aspose.Words de aynı şeyi sizin için yapar.

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

* Enum [AutoFitBehavior](../../autofitbehavior/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
