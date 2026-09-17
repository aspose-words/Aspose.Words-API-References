---
title: "Méthode Aspose::Words::Layout::LayoutOptions::get_RevisionOptions"
linktitle: "get_RevisionOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Layout::LayoutOptions::get_RevisionOptions. Obtient les options de révision en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.layout/layoutoptions/get_revisionoptions/
---
## LayoutOptions::get_RevisionOptions method


Obtient les options de révision.

```cpp
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> Aspose::Words::Layout::LayoutOptions::get_RevisionOptions() const
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

* Class [RevisionOptions](../../revisionoptions/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
