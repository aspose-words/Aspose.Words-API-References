---
title: "Aspose::Words::Tables::RowFormat::get_HeadingFormat yöntemi"
linktitle: "get_HeadingFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::RowFormat::get_HeadingFormat yöntemi. Tablo birden fazla sayfaya yayıldığında, satır her sayfada tablo başlığı olarak tekrarlanıyorsa doğru (C++)."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


Tablo birden fazla sayfaya yayıldığında satır her sayfada tablo başlığı olarak tekrarlanıyorsa doğru.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## Örnekler



Her sayfada tekrarlanan satırlarla bir tablo oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// "HeadingFormat" bayrağı "true" olarak ayarlanmışken eklenen tüm satırlar
// tablonun kapsadığı her sayfanın üst kısmında görünecektir.
builder->get_RowFormat()->set_HeadingFormat(true);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_CellFormat()->set_Width(100);
builder->InsertCell();
builder->Write(u"Heading row 1");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Heading row 2");
builder->EndRow();

builder->get_CellFormat()->set_Width(50);
builder->get_ParagraphFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeadingFormat(false);

// Tablonun iki sayfaya yayılması için yeterli sayıda satır ekleyin.
for (int32_t i = 0; i < 50; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 1.", table->get_Rows()->get_Count()));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 2.", table->get_Rows()->get_Count()));
    builder->EndRow();
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableSetHeadingRow.docx");
```

## Ayrıca Bakınız

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
