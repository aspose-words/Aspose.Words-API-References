---
title: "Aspose::Words::Tables::CellFormat::SetPaddings méthode"
linktitle: "SetPaddings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::CellFormat::SetPaddings méthode. Définit la quantité d'espace (en points) à ajouter à gauche/haut/droite/bas du contenu de la cellule en C++."
type: docs
weight: 31000
url: /fr/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


Définit la quantité d'espace (en points) à ajouter à gauche/haut/droite/bas du contenu de la cellule.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## Exemples



Montre comment ajouter des espaces au contenu d'une cellule.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Définissez une distance de remplissage (en points) entre la bordure et le contenu du texte
// de chaque cellule de tableau que nous créons avec le générateur de documents.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// Créez un tableau avec une cellule dont le contenu aura un remplissage d'espaces.
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## Voir aussi

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
