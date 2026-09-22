---
title: "Aspose::Words::Tables::RowFormat::get_HeightRule yöntemi"
linktitle: "get_HeightRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::RowFormat::get_HeightRule yöntemi. C++'ta tablo satırının yüksekliğini belirleme kuralını alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.tables/rowformat/get_heightrule/
---
## RowFormat::get_HeightRule method


Tablo satırının yüksekliğini belirleme kuralını alır veya ayarlar.

```cpp
Aspose::Words::HeightRule Aspose::Words::Tables::RowFormat::get_HeightRule()
```


## Örnekler



Bir biçimlendirilmiş tablo oluşturmanın [DocumentBuilder](../../../aspose.words/documentbuilder/) kullanılarak nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// Metin ve tablo görünümü için bazı biçimlendirme seçenekleri ayarlayın.
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// Bir belge oluşturucuda biçimlendirme seçeneklerini yapılandırmak, bunları uygular
// imlecin bulunduğu mevcut hücre/ satıra,
// ve aynı zamanda o oluşturucu kullanılarak oluşturulan yeni hücre ve satırlara da.
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// Oluşturmak üzere olduğumuz yeni satır ve hücreler için oluşturucunun biçimlendirme nesnelerini yeniden yapılandırın.
// Builder bu öğeleri zaten oluşturulmuş ilk satıra uygulamayacak, böylece başlık satırı olarak öne çıkacaktır.
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```


Bir belge oluşturucu ile satırların nasıl biçimlendirileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// İkinci bir satır başlatın ve ardından yüksekliğini yapılandırın. Oluşturucu bu ayarları şuraya uygulayacaktır
// mevcut satırına ve sonradan oluşturacağı yeni satırlara.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// İlk satır, dolgu yeniden yapılandırmasından etkilenmedi ve hâlâ varsayılan değerleri tutmaktadır.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Ayrıca Bakınız

* Enum [HeightRule](../../../aspose.words/heightrule/)
* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
