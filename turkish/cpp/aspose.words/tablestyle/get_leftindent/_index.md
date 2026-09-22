---
title: "Aspose::Words::TableStyle::get_LeftIndent yöntemi"
linktitle: "get_LeftIndent"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::TableStyle::get_LeftIndent yöntemi. C++'da bir tablonun sol girintisini temsil eden değeri alır veya ayarlar."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/tablestyle/get_leftindent/
---
## TableStyle::get_LeftIndent method


Bir tablonun sol girintisini temsil eden değeri alır veya ayarlar.

```cpp
double Aspose::Words::TableStyle::get_LeftIndent()
```


## Örnekler



Bir tablonun konumunu nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aşağıda bir tabloyu yatay olarak hizalamanın iki yolu verilmiştir.
// 1 -  \"Alignment\" özelliğini kullanarak sayfadaki bir konuma, örneğin merkeze hizalayın:
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

// Bir tablo ekleyin ve oluşturduğumuz stili ona uygulayın.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  \"LeftIndent\" özelliğini kullanarak sayfanın sol kenar boşluğundan bir girinti belirtin:
tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle2"));
tableStyle->set_LeftIndent(55);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Green());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned according to left indent");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

doc->Save(get_ArtifactsDir() + u"Table.SetTableAlignment.docx");
```

## Ayrıca Bakınız

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
