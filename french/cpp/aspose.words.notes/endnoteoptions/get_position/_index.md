---
title: "Aspose::Words::Notes::EndnoteOptions::get_Position méthode"
linktitle: "get_Position"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Notes::EndnoteOptions::get_Position méthode. Spécifie la position des notes de fin en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.notes/endnoteoptions/get_position/
---
## EndnoteOptions::get_Position method


Spécifie la position des notes de fin.

```cpp
Aspose::Words::Notes::EndnotePosition Aspose::Words::Notes::EndnoteOptions::get_Position()
```


## Exemples



Montre comment sélectionner un autre emplacement où le document collecte et affiche ses notes de fin.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Une note de fin est un moyen d'attacher une référence ou un commentaire marginal au texte
// qui n'interfère pas avec le flux du texte principal.
// L'insertion d'une note de fin ajoute un petit symbole de référence en exposant
// dans le texte principal où nous insérons la note de fin.
// Chaque note de fin crée également une entrée à la fin du document, composée d'un symbole
// qui correspond au symbole de référence dans le texte principal.
// Le texte de référence que nous passons à la méthode "InsertEndnote" du document builder.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// Nous pouvons utiliser la propriété "Position" pour déterminer où le document placera toutes ses notes de fin.
// Si nous définissons la valeur de la propriété "Position" sur "EndnotePosition.EndOfDocument",
// toutes les notes de bas de page apparaîtront dans une collection à la fin du document. C'est la valeur par défaut.
// Si nous définissons la valeur de la propriété "Position" sur "EndnotePosition.EndOfSection",
// toutes les notes de bas de page apparaîtront dans une collection à la fin de la section dont le texte contient la marque de référence de la note de fin.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```

## Voir aussi

* Enum [EndnotePosition](../../endnoteposition/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
