---
title: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition méthode"
linktitle: "get_RevisionBarsPosition"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition méthode. Obtient ou définit la position de rendu des barres de révision. La valeur par défaut est Outside en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.layout/revisionoptions/get_revisionbarsposition/
---
## RevisionOptions::get_RevisionBarsPosition method


Obtient ou définit la position de rendu des barres de révision. La valeur par défaut est [Outside](../../../aspose.words.drawing/horizontalalignment/).

```cpp
Aspose::Words::Drawing::HorizontalAlignment Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition() const
```


## Exemples



Montre comment modifier l'apparence des révisions dans un document de sortie rendu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez une révision, puis changez la couleur de toutes les révisions en vert.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Supprimez la barre qui apparaît à gauche de chaque ligne révisée.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Voir aussi

* Enum [HorizontalAlignment](../../../aspose.words.drawing/horizontalalignment/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
