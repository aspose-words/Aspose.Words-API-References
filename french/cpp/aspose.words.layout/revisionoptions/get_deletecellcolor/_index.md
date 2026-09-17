---
title: "Méthode Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor"
linktitle: "get_DeleteCellColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor méthode. Permet de spécifier la couleur à utiliser pour les cellules supprimées Deletion. La valeur par défaut est Pink en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words.layout/revisionoptions/get_deletecellcolor/
---
## RevisionOptions::get_DeleteCellColor method


Permet de spécifier la couleur à utiliser pour les cellules supprimées [Deletion](../../../aspose.words/revisiontype/). La valeur par défaut est [Pink](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor()
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
