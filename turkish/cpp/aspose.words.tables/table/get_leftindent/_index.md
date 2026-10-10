---
title: "Aspose::Words::Tables::Table::get_LeftIndent yöntemi"
linktitle: "get_LeftIndent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_LeftIndent yöntemi. Tabloyun sol girintisini temsil eden değeri alır veya ayarlar (C++)."
type: docs
weight: 26000
url: /tr/cpp/aspose.words.tables/table/get_leftindent/
---
## Table::get_LeftIndent method


Tablonun sol girintisini temsil eden değeri alır veya ayarlar.

```cpp
double Aspose::Words::Tables::Table::get_LeftIndent()
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

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
