---
title: "Aspose::Words::Tables::CellFormat sınıfı"
linktitle: "CellFormat"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::CellFormat sınıfı. Bir tablo hücresinin tüm biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.tables/cellformat/
---
## CellFormat class


Bir tablo hücresinin tüm biçimlendirmesini temsil eder. Daha fazla bilgi edinmek için [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/) dokümantasyon makalesini ziyaret edin.

```cpp
class CellFormat : public Aspose::Words::IBorderAttrSource,
                   public Aspose::Words::IShadingAttrSource
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Hücreyi varsayılan biçimlendirmeye sıfırlar. Hücrenin genişliğini değiştirmez. |
| [get_Borders](./get_borders/)() | Hücrenin kenarlık koleksiyonunu alır. |
| [get_BottomPadding](./get_bottompadding/)() | Hücre içeriğinin altına eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [get_FitText](./get_fittext/)() | Eğer **true** ise, metni hücreye sığdırır, her paragrafı hücrenin genişliğine sıkıştırır. |
| [get_HideMark](./get_hidemark/)() | Hücre işaretinin görünürlüğünü döndürür. |
| [get_HorizontalMerge](./get_horizontalmerge/)() | Hücrenin satırdaki diğer hücrelerle yatay olarak nasıl birleştirileceğini belirtir. |
| [get_LeftPadding](./get_leftpadding/)() | Hücre içeriğinin soluna eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [get_Orientation](./get_orientation/)() | Bir tablo hücresindeki metnin yönünü alır veya ayarlar. |
| [get_PreferredWidth](./get_preferredwidth/)() | Hücrenin tercih edilen genişliğini alır veya ayarlar. |
| [get_RightPadding](./get_rightpadding/)() | Hücre içeriğinin sağına eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [get_Shading](./get_shading/)() | Hücre için gölgelendirme biçimlendirmesine referans veren bir [Shading](../../aspose.words/shading/) nesnesi döndürür. |
| [get_TopPadding](./get_toppadding/)() | Hücre içeriğinin üstüne eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Hücredeki metnin dikey hizalamasını alır veya ayarlar. |
| [get_VerticalMerge](./get_verticalmerge/)() | Hücrenin diğer hücrelerle dikey olarak nasıl birleştirildiğini belirtir. |
| [get_Width](./get_width/)() | Hücrenin genişliğini puan cinsinden alır. |
| [get_WrapText](./get_wraptext/)() | Eğer **true** ise, hücre için metni kaydır. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BottomPadding](./set_bottompadding/)(double) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_BottomPadding](./get_bottompadding/). |
| [set_FitText](./set_fittext/)(bool) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_FitText](./get_fittext/). |
| [set_HideMark](./set_hidemark/)(bool) | Hücre işaretinin görünürlüğünü ayarlar. |
| [set_HorizontalMerge](./set_horizontalmerge/)(Aspose::Words::Tables::CellMerge) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_HorizontalMerge](./get_horizontalmerge/). |
| [set_LeftPadding](./set_leftpadding/)(double) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_LeftPadding](./get_leftpadding/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::TextOrientation) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_Orientation](./get_orientation/). |
| [set_PreferredWidth](./set_preferredwidth/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_PreferredWidth](./get_preferredwidth/). |
| [set_RightPadding](./set_rightpadding/)(double) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_RightPadding](./get_rightpadding/). |
| [set_TopPadding](./set_toppadding/)(double) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_TopPadding](./get_toppadding/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::Tables::CellVerticalAlignment) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_VerticalAlignment](./get_verticalalignment/). |
| [set_VerticalMerge](./set_verticalmerge/)(Aspose::Words::Tables::CellMerge) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_VerticalMerge](./get_verticalmerge/). |
| [set_Width](./set_width/)(double) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_Width](./get_width/). |
| [set_WrapText](./set_wraptext/)(bool) | Ayarlayıcı [Aspose::Words::Tables::CellFormat::get_WrapText](./get_wraptext/). |
| [SetPaddings](./setpaddings/)(double, double, double, double) | Hücre içeriğinin sol/üst/sağ/alt kısmına eklenmesi gereken boşluk miktarını (puan cinsinden) ayarlar. |
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


Bir tablo hücresinin biçimlendirmesini nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

// Bir hücrenin görünümünü değiştiren biçimlendirmeyi ayarlamak için hücrenin "CellFormat" özelliğini kullanın.
firstCell->get_CellFormat()->set_Width(30);
firstCell->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
firstCell->get_CellFormat()->get_Shading()->set_ForegroundPatternColor(System::Drawing::Color::get_LightGreen());

doc->Save(get_ArtifactsDir() + u"Table.CellFormat.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
