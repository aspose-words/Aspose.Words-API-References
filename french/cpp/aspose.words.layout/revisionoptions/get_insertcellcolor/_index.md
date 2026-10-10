---
title: "Méthode Aspose::Words::Layout::RevisionOptions::get_InsertCellColor"
linktitle: "get_InsertCellColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Layout::RevisionOptions::get_InsertCellColor. Permet de spécifier la couleur à utiliser pour les cellules insérées Insertion. La valeur par défaut est Blue en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words.layout/revisionoptions/get_insertcellcolor/
---
## RevisionOptions::get_InsertCellColor method


Permet de spécifier la couleur à utiliser pour les cellules insérées [Insertion](../../../aspose.words/revisiontype/). La valeur par défaut est [Blue](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertCellColor()
```


## Exemples



Montre comment travailler avec la couleur de révision des cellules d’insertion/suppression.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Cell revisions.docx");

doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertCellColor(Aspose::Words::Layout::RevisionColor::LightBlue);
doc->get_LayoutOptions()->get_RevisionOptions()->set_DeleteCellColor(Aspose::Words::Layout::RevisionColor::DarkRed);

doc->Save(get_ArtifactsDir() + u"Revision.RevisionCellColor.pdf");
```

## Voir aussi

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
