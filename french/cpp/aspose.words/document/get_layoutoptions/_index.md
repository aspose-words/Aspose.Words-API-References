---
title: "Aspose::Words::Document::get_LayoutOptions méthode"
linktitle: "get_LayoutOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_LayoutOptions méthode. Obtient un objet LayoutOptions qui représente les options permettant de contrôler le processus de mise en page de ce document en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words/document/get_layoutoptions/
---
## Document::get_LayoutOptions method


Obtient un objet [LayoutOptions](../../../aspose.words.layout/layoutoptions/) qui représente les options permettant de contrôler le processus de mise en page de ce document.

```cpp
System::SharedPtr<Aspose::Words::Layout::LayoutOptions> Aspose::Words::Document::get_LayoutOptions() const
```


## Exemples



Montre comment masquer du texte dans un document de sortie rendu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insérez du texte masqué, puis spécifiez si nous souhaitons l'omettre d'un document rendu.
builder->Writeln(u"This text is not hidden.");
builder->get_Font()->set_Hidden(true);
builder->Writeln(u"This text is hidden.");

doc->get_LayoutOptions()->set_ShowHiddenText(showHiddenText);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsHiddenText.pdf");
```


Montre comment afficher les marques de paragraphe dans un document de sortie rendu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez quelques paragraphes, puis activez les marques de paragraphe pour afficher la fin des paragraphes
// avec le symbole pilcrow (¶) lorsque nous rendons le document.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

doc->get_LayoutOptions()->set_ShowParagraphMarks(showParagraphMarks);

doc->Save(get_ArtifactsDir() + u"Document.LayoutOptionsParagraphMarks.pdf");
```


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

* Class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
