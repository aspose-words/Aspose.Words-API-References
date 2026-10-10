---
title: "Aspose::Words::Tables::CellFormat::get_Shading metodu"
linktitle: "get_Shading"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellFormat::get_Shading metodu. Hücre için gölgelendirme biçimlendirmesine referans veren bir Shading nesnesi döndürür C++'da."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.tables/cellformat/get_shading/
---
## CellFormat::get_Shading method


Hücre için gölgelendirme biçimlendirmesine referans veren bir [Shading](../../../aspose.words/shading/) nesnesi döndürür.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Tables::CellFormat::get_Shading()
```


## Örnekler



Özel kenarlıklarla bir tablo oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// Bir DocumentBuilder için tablo biçimlendirme seçeneklerini ayarlama
// Bunları, onunla eklediğimiz her satır ve hücreye uygular.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// Biçimlendirmeyi değiştirmek, mevcut hücreye uygulanır,
// ve ardından builder ile oluşturduğumuz yeni hücrelere de.
// Bu, daha önce eklediğimiz hücreleri etkilemez.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// Dikey metni sığdırmak için satır yüksekliğini artırın.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


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

## Ayrıca Bakınız

* Class [Shading](../../../aspose.words/shading/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
