---
title: "Méthode Aspose::Words::Tables::RowFormat::get_HeadingFormat"
linktitle: "get_HeadingFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Tables::RowFormat::get_HeadingFormat. Vrai si la ligne est répétée comme en-tête de tableau sur chaque page lorsque le tableau s'étend sur plus d'une page en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.tables/rowformat/get_headingformat/
---
## RowFormat::get_HeadingFormat method


Vrai si la ligne est répétée comme en-tête de table sur chaque page lorsque la table s'étend sur plusieurs pages.

```cpp
bool Aspose::Words::Tables::RowFormat::get_HeadingFormat()
```


## Exemples



Montre comment créer un tableau avec des lignes qui se répètent sur chaque page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Toutes les lignes insérées pendant que le drapeau "HeadingFormat" est réglé sur "true"
// apparaîtront en haut du tableau sur chaque page qu'il couvre.
builder->get_RowFormat()->set_HeadingFormat(true);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_CellFormat()->set_Width(100);
builder->InsertCell();
builder->Write(u"Heading row 1");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Heading row 2");
builder->EndRow();

builder->get_CellFormat()->set_Width(50);
builder->get_ParagraphFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeadingFormat(false);

// Ajoutez suffisamment de lignes pour que le tableau s'étende sur deux pages.
for (int32_t i = 0; i < 50; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 1.", table->get_Rows()->get_Count()));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, column 2.", table->get_Rows()->get_Count()));
    builder->EndRow();
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableSetHeadingRow.docx");
```

## Voir aussi

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
