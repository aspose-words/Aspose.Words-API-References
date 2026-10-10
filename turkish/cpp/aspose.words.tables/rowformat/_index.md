---
title: "Aspose::Words::Tables::RowFormat class"
linktitle: "RowFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::RowFormat class. Bir tablo satırı için tüm biçimlendirmeyi temsil eder. Daha fazla bilgi için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.tables/rowformat/
---
## RowFormat class


Bir tablo satırının tüm biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) dokümantasyon makalesini ziyaret edin.

```cpp
class RowFormat : public Aspose::Words::IBorderAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Satır biçimlendirmesini varsayılanlara sıfırlar. |
| [get_AllowBreakAcrossPages](./get_allowbreakacrosspages/)() | Bir tablo satırındaki metnin sayfa sonu boyunca bölünmesine izin veriliyorsa doğru. |
| [get_Borders](./get_borders/)() | Satır için varsayılan hücre kenarlıklarının koleksiyonunu alır. |
| [get_HeadingFormat](./get_headingformat/)() | Tablo birden fazla sayfaya yayıldığında satır her sayfada tablo başlığı olarak tekrarlanıyorsa doğru. |
| [get_Height](./get_height/)() | Tablo satırının yüksekliğini puan cinsinden alır veya ayarlar. |
| [get_HeightRule](./get_heightrule/)() | Tablo satırının yüksekliğini belirleme kuralını alır veya ayarlar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowBreakAcrossPages](./set_allowbreakacrosspages/)(bool) | Ayarlayıcı [Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages](./get_allowbreakacrosspages/). |
| [set_HeadingFormat](./set_headingformat/)(bool) | Ayarlayıcı [Aspose::Words::Tables::RowFormat::get_HeadingFormat](./get_headingformat/). |
| [set_Height](./set_height/)(double) | [Aspose::Words::Tables::RowFormat::get_Height](./get_height/) için ayarlayıcı. |
| [set_HeightRule](./set_heightrule/)(Aspose::Words::HeightRule) | [Aspose::Words::Tables::RowFormat::get_HeightRule](./get_heightrule/) için ayarlayıcı. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
