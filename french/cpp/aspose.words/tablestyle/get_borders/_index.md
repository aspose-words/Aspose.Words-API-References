---
title: "Aspose::Words::TableStyle::get_Borders méthode"
linktitle: "get_Borders"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::TableStyle::get_Borders méthode. Obtient la collection des bordures de cellule par défaut pour le style en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words/tablestyle/get_borders/
---
## TableStyle::get_Borders method


Obtient la collection des bordures de cellules par défaut pour le style.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::TableStyle::get_Borders()
```


## Exemples



Montre comment créer des paramètres de style personnalisés pour le tableau.
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

// La définition des propriétés de style d'un tableau peut affecter les propriétés du tableau lui‑même.
ASSERT_FALSE(table->get_Bidi());
ASPOSE_ASSERT_EQ(5.0, table->get_CellSpacing());
ASSERT_EQ(u"MyTableStyle1", table->get_StyleName());

doc->Save(get_ArtifactsDir() + u"Table.TableStyleCreation.docx");
```

## Voir aussi

* Class [BorderCollection](../../bordercollection/)
* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
