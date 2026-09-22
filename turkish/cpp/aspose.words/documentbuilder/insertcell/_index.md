---
title: "Aspose::Words::DocumentBuilder::InsertCell method"
linktitle: "InsertCell"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBuilder::InsertCell method. C++'ta belgeye bir tablo hücresi ekler."
type: docs
weight: 29000
url: /tr/cpp/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder::InsertCell method


Belgeye bir tablo hücresi ekler.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::DocumentBuilder::InsertCell()
```


### ReturnValue

Az önce eklenen hücre düğümü.
## Açıklamalar


Bir tablo başlatmak için sadece [InsertCell](./) metodunu çağırın. Bundan sonra, [DocumentBuilder](../) sınıfının diğer metodlarını kullanarak eklediğiniz tüm içerik mevcut hücreye eklenecektir.

Aynı satırda yeni bir hücre başlatmak için, [InsertCell](./) metodunu tekrar çağırın.

Bir tablo satırını sonlandırmak için [EndRow](../endrow/) metodunu çağırın.

Hücre biçimlendirmesini belirtmek için [CellFormat](../get_cellformat/) özelliğini kullanın.

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


Bir document builder kullanarak tablo oluşturmanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Tabloyu başlatın, ardından ilk satırı iki hücreyle doldurun.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// Call the builder's "EndRow" method to start a new row.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## Ayrıca Bakınız

* Class [Cell](../../../aspose.words.tables/cell/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
