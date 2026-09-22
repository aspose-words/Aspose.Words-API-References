---
title: "Aspose::Words::Tables::Table::get_CellSpacing yöntemi"
linktitle: "get_CellSpacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_CellSpacing yöntemi. Hücreler arasındaki boşluk miktarını (nokta cinsinden) C++'da alır veya ayarlar."
type: docs
weight: 17000
url: /tr/cpp/aspose.words.tables/table/get_cellspacing/
---
## Table::get_CellSpacing method


Hücreler arasındaki boşluk miktarını (puan cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::Tables::Table::get_CellSpacing()
```


## Örnekler



Bir tabloda bireysel hücreler arasındaki boşluğu nasıl etkinleştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Animal");
builder->InsertCell();
builder->Write(u"Class");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Dog");
builder->InsertCell();
builder->Write(u"Mammal");
builder->EndTable();

table->set_CellSpacing(3);

// Hücreler arasındaki boşluğu etkinleştirmek için "AllowCellSpacing" özelliğini "true" olarak ayarlayın
// "CellSpacing" özelliğinin değeri kadar bir büyüklükte, puan cinsinden.
// Hücre boşluğunu devre dışı bırakmak için "AllowCellSpacing" özelliğini "false" olarak ayarlayın
// ve "CellSpacing" özelliğinin değerini yok sayın.
table->set_AllowCellSpacing(allowCellSpacing);

doc->Save(get_ArtifactsDir() + u"Table.AllowCellSpacing.html");

// "CellSpacing" özelliğini ayarlamak, hücre boşluğunu otomatik olarak etkinleştirir.
table->set_CellSpacing(5);

ASSERT_TRUE(table->get_AllowCellSpacing());
```


Tablo için özel stil ayarlarının nasıl oluşturulacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Name");
builder->InsertCell();
builder->Write(u"مرحبًا");
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_AllowBreakAcrossPages(true);
tableStyle->set_CellSpacing(5);
tableStyle->set_BottomPadding(20);
tableStyle->set_LeftPadding(5);
tableStyle->set_RightPadding(10);
tableStyle->set_TopPadding(20);
tableStyle->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AntiqueWhite());
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
tableStyle->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);

table->set_Style(tableStyle);

// Bir tablonun stil özelliklerini ayarlamak, tablonun kendi özelliklerini etkileyebilir.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
