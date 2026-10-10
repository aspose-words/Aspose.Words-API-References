---
title: "Méthode Aspose::Words::DocumentBuilder::MoveToCell"
linktitle: "MoveToCell"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::MoveToCell. Déplace le curseur vers une cellule de tableau dans la section actuelle en C++."
type: docs
weight: 53000
url: /fr/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


Déplace le curseur vers une cellule de tableau dans la section actuelle.

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| tableIndex | int32_t | L'index du tableau vers lequel se déplacer. |
| rowIndex | int32_t | L'index de la ligne dans le tableau. |
| columnIndex | int32_t | L'index de la colonne dans le tableau. |
| characterIndex | int32_t | L'index du caractère à l'intérieur de la cellule. Une valeur négative vous permet de spécifier une position depuis la fin de la cellule. Utilisez -1 pour vous déplacer à la fin de la cellule. |
## Remarques


La navigation est effectuée à l'intérieur de l'histoire actuelle de la section en cours.

Pour les paramètres d'index, lorsque l'index est supérieur ou égal à 0, il indique un index à partir du début, 0 étant le premier élément. Lorsque l'index est inférieur à 0, il indique un index depuis la fin, -1 étant le dernier élément.

## Exemples



Montre comment déplacer le curseur d'un DocumentBuilder vers une cellule d'un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez un tableau 2x2 vide.
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// Parce que nous avons terminé le tableau avec la méthode EndTable,
// le curseur du DocumentBuilder se trouve actuellement à l'extérieur du tableau.
// Ce curseur a la même fonction que le curseur clignotant de texte de Microsoft Word.
// Il peut également être déplacé vers un autre emplacement dans le document en utilisant les méthodes MoveTo du DocumentBuilder.
// Nous pouvons ramener le curseur à l'intérieur du tableau vers une cellule spécifique.
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## Voir aussi

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
