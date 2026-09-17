---
title: "Méthode Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor"
linktitle: "get_InsertedTextColor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor. Permet de spécifier la couleur à utiliser pour le contenu inséré Insertion. La valeur par défaut est ByAuthor en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.layout/revisionoptions/get_insertedtextcolor/
---
## RevisionOptions::get_InsertedTextColor method


Permet de spécifier la couleur à utiliser pour le contenu inséré [Insertion](../../../aspose.words/revisiontype/). La valeur par défaut est [ByAuthor](../../revisioncolor/).

```cpp
Aspose::Words::Layout::RevisionColor Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor()
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

* Enum [RevisionColor](../../revisioncolor/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
