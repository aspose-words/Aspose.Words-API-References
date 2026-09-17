---
title: "Aspose::Words::Notes::FootnoteOptions::get_Position méthode"
linktitle: "get_Position"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::FootnoteOptions::get_Position méthode. Spécifie la position des notes de bas de page en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.notes/footnoteoptions/get_position/
---
## FootnoteOptions::get_Position method


Spécifie la position des notes de bas de page.

```cpp
Aspose::Words::Notes::FootnotePosition Aspose::Words::Notes::FootnoteOptions::get_Position()
```


## Exemples



Montre comment sélectionner un autre emplacement où le document collecte et affiche ses notes de bas de page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Une note de bas de page est un moyen d'attacher une référence ou un commentaire marginal au texte
// qui n'interfère pas avec le flux du texte principal.
// Insérer une note de bas de page ajoute un petit symbole de référence en exposant
// dans le texte principal où nous insérons la note de bas de page.
// Chaque note de bas de page crée également une entrée en bas de la page, composée d'un symbole
// qui correspond au symbole de référence dans le texte principal.
// Le texte de référence que nous transmettons à la méthode "InsertFootnote" du constructeur de document.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// Nous pouvons utiliser la propriété "Position" pour déterminer où le document placera toutes ses notes de bas de page.
// Si nous définissons la valeur de la propriété "Position" sur "FootnotePosition.BottomOfPage",
// toute note de bas de page apparaîtra en bas de la page qui contient son repère de référence. C'est la valeur par défaut.
// Si nous définissons la valeur de la propriété "Position" sur "FootnotePosition.BeneathText",
// toute note de bas de page apparaîtra à la fin du texte de la page qui contient son repère de référence.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```

## Voir aussi

* Enum [FootnotePosition](../../footnoteposition/)
* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
