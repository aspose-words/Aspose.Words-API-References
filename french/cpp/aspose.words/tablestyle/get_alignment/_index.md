---
title: "Méthode Aspose::Words::TableStyle::get_Alignment"
linktitle: "get_Alignment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::TableStyle::get_Alignment. Spécifie l'alignement du style de tableau en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/tablestyle/get_alignment/
---
## TableStyle::get_Alignment method


Spécifie l'alignement du style de tableau.

```cpp
Aspose::Words::Tables::TableAlignment Aspose::Words::TableStyle::get_Alignment()
```


## Exemples



Montre comment définir la position d'un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ci-dessous deux façons d'aligner un tableau horizontalement.
// 1 -  Utilisez la propriété "Alignment" pour l'aligner à un emplacement sur la page, comme le centre :
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->set_Alignment(Aspose::Words::Tables::TableAlignment::Center);
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Blue());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Single);

// Insérez un tableau et appliquez-lui le style que nous avons créé.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Aligned to the center of the page");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

table->set_Style(tableStyle);

// 2 -  Utilisez la propriété "LeftIndent" pour spécifier une indentation depuis la marge gauche de la page :
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

## Voir aussi

* Enum [TableAlignment](../../../aspose.words.tables/tablealignment/)
* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
