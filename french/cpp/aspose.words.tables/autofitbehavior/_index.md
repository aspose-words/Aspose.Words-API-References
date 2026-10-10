---
title: "Aspose::Words::Tables::AutoFitBehavior enum"
linktitle: "AutoFitBehavior"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::AutoFitBehavior enum. Détermine comment Aspose.Words redimensionne le tableau lorsque vous appelez la méthode AutoFit() en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.tables/autofitbehavior/
---
## AutoFitBehavior enum


Détermine comment Aspose.Words redimensionne le tableau lorsque vous appelez la méthode [AutoFit()](../table/autofit/).

```cpp
enum class AutoFitBehavior
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| AutoFitToContents | 0 | Aspose.Words active l'option AutoFit, supprime la largeur préférée du tableau et de toutes les cellules, puis met à jour la disposition du tableau. Dans le tableau résultant, les largeurs des cellules sont ajustées pour s'adapter au contenu du tableau. Le tableau rétrécira très probablement. |
| AutoFitToWindow | 1 | Lorsque vous utilisez cette valeur, Aspose.Words active l'option AutoFit, définit la largeur préférée du tableau à 100 %, supprime les largeurs préférées de toutes les cellules, puis met à jour la disposition du tableau. En conséquence, le tableau occupe toute la largeur disponible et les largeurs des cellules sont ajustées pour s'adapter au contenu du tableau. |
| FixedColumnWidths | 2 | Aspose.Words désactive l'option AutoFit et supprime la largeur préférée du tableau. Les largeurs des cellules restent telles qu'elles sont spécifiées par leurs propriétés [Width](../cellformat/get_width/). |


## Exemples



Montre comment créer un nouveau tableau tout en appliquant un style.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Nous devons insérer au moins une ligne avant de définir tout format de tableau.
builder->InsertCell();

// Définissez le style de tableau utilisé en fonction de l'identifiant du style.
// Notez que tous les styles de tableau ne sont pas disponibles lors de l'enregistrement au format .doc.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Appliquez partiellement le style aux caractéristiques du tableau en fonction des prédicats, puis construisez le tableau.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```


Montre comment créer un tableau formaté 2x2.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();

// Lors de la création du tableau, le constructeur de document appliquera les valeurs actuelles de ses propriétés RowFormat/CellFormat.
// à la ligne/colonne actuelle où se trouve le curseur ainsi qu'aux nouvelles lignes/colonnes créées.
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(0)->get_CellFormat()->get_VerticalAlignment());
ASSERT_EQ(Aspose::Words::Tables::CellVerticalAlignment::Center, table->get_Rows()->idx_get(0)->get_Cells()->idx_get(1)->get_CellFormat()->get_VerticalAlignment());

builder->InsertCell();
builder->get_RowFormat()->set_Height(100);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 2, cell 2.");
builder->EndRow();
builder->EndTable();

// Les lignes et cellules ajoutées précédemment ne sont pas affectées rétroactivement par les modifications du formatage du constructeur.
ASPOSE_ASSERT_EQ(0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());
ASPOSE_ASSERT_EQ(100, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());
ASSERT_EQ(Aspose::Words::TextOrientation::Upward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(0)->get_CellFormat()->get_Orientation());
ASSERT_EQ(Aspose::Words::TextOrientation::Downward, table->get_Rows()->idx_get(1)->get_Cells()->idx_get(1)->get_CellFormat()->get_Orientation());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.BuildTable.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
