---
title: "Aspose::Words::Tables::Row::get_RowFormat method"
linktitle: "get_RowFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Row::get_RowFormat method. C++'ta satırın biçimlendirme özelliklerine erişim sağlar."
type: docs
weight: 12000
url: /tr/cpp/aspose.words.tables/row/get_rowformat/
---
## Row::get_RowFormat method


Satırın biçimlendirme özelliklerine erişim sağlar.

```cpp
System::SharedPtr<Aspose::Words::Tables::RowFormat> Aspose::Words::Tables::Row::get_RowFormat()
```


## Örnekler



Bir tabloda satırların ve hücrelerin biçimini nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"City");
builder->InsertCell();
builder->Write(u"Country");
builder->EndRow();
builder->InsertCell();
builder->Write(u"London");
builder->InsertCell();
builder->Write(u"U.K.");
builder->EndTable();

// İlk satırın "RowFormat" özelliğini biçimlendirmeyi değiştirmek için kullanın
// bu satırdaki tüm hücrelerin içeriğinin.
System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = table->get_FirstRow()->get_RowFormat();
rowFormat->set_Height(25);
rowFormat->get_Borders()->idx_get(Aspose::Words::BorderType::Bottom)->set_Color(System::Drawing::Color::get_Red());

// Son satırdaki ilk hücrenin "CellFormat" özelliğini, o hücrenin içeriğinin biçimini değiştirmek için kullanın.
System::SharedPtr<Aspose::Words::Tables::CellFormat> cellFormat = table->get_LastRow()->get_FirstCell()->get_CellFormat();
cellFormat->set_Width(100);
cellFormat->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());

doc->Save(get_ArtifactsDir() + u"Table.RowCellFormat.docx");
```


Bir tablo satırının biçimini nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// İlk satırın "RowFormat" özelliğini, tüm satırın görünümünü değiştiren biçimlendirmeyi ayarlamak için kullanın.
System::SharedPtr<Aspose::Words::Tables::Row> firstRow = table->get_FirstRow();
firstRow->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::None);
firstRow->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
firstRow->get_RowFormat()->set_AllowBreakAcrossPages(true);

doc->Save(get_ArtifactsDir() + u"Table.RowFormat.docx");
```

## Ayrıca Bakınız

* Class [RowFormat](../../rowformat/)
* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
