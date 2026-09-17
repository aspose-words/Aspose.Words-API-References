---
title: "Aspose::Words::HeightRule enum"
linktitle: "HeightRule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::HeightRule enum. Spécifie la règle de détermination de la hauteur d’un objet en C++."
type: docs
weight: 91000
url: /fr/cpp/aspose.words/heightrule/
---
## HeightRule enum


Spécifie la règle de détermination de la hauteur d'un objet.

```cpp
enum class HeightRule
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| AtLeast | 0 | La hauteur sera au moins la hauteur spécifiée en points. Elle augmentera, si nécessaire, pour accueillir tout le texte à l’intérieur d’un objet. |
| Exactly | 1 | La hauteur est spécifiée exactement en points. Veuillez noter que si le texte ne peut pas tenir dans l’objet de cette hauteur, il sera tronqué. |
| Auto | 2 | La hauteur augmentera automatiquement pour accueillir tout le texte à l’intérieur d’un objet. |


## Exemples



Montre comment formater des lignes avec un constructeur de document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");

// Commencez une deuxième ligne, puis configurez sa hauteur. Le constructeur appliquera ces paramètres à
// sa ligne actuelle, ainsi qu’à toutes les nouvelles lignes qu’il crée par la suite.
builder->EndRow();

System::SharedPtr<Aspose::Words::Tables::RowFormat> rowFormat = builder->get_RowFormat();
rowFormat->set_Height(100);
rowFormat->set_HeightRule(Aspose::Words::HeightRule::Exactly);

builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->EndTable();

// La première ligne n’a pas été affectée par la reconfiguration du remplissage et conserve toujours les valeurs par défaut.
ASPOSE_ASSERT_EQ(0.0, table->get_Rows()->idx_get(0)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Auto, table->get_Rows()->idx_get(0)->get_RowFormat()->get_HeightRule());

ASPOSE_ASSERT_EQ(100.0, table->get_Rows()->idx_get(1)->get_RowFormat()->get_Height());
ASSERT_EQ(Aspose::Words::HeightRule::Exactly, table->get_Rows()->idx_get(1)->get_RowFormat()->get_HeightRule());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
