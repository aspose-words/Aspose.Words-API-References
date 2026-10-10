---
title: "Aspose::Words::Tables::CellFormat::SetPaddings metodu"
linktitle: "SetPaddings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellFormat::SetPaddings metodu. Hücre içeriğinin sol/üst/sağ/alt kısmına eklenmesi gereken boşluk miktarını (nokta cinsinden) C++'da ayarlar."
type: docs
weight: 31000
url: /tr/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


Hücre içeriğinin sol/üst/sağ/alt kısmına eklenmesi gereken boşluk miktarını (puan cinsinden) ayarlar.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## Örnekler



Bir hücrenin içeriğini boşluk karakteriyle doldurmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Kenarlık ile metin içeriği arasına (nokta cinsinden) bir dolgu mesafesi ayarlayın
// belge oluşturucu ile oluşturduğumuz her tablo hücresinin.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// İçeriği boşluk dolgusuna sahip olacak bir hücreli bir tablo oluşturun.
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## Ayrıca Bakınız

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
