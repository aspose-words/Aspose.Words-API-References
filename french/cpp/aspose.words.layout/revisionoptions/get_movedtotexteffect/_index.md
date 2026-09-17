---
title: "Méthode Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect"
linktitle: "get_MovedToTextEffect"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect. Permet de spécifier l'effet à appliquer aux zones où le contenu a été déplacé Moving. La valeur par défaut est DoubleUnderline en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.layout/revisionoptions/get_movedtotexteffect/
---
## RevisionOptions::get_MovedToTextEffect method


Permet de spécifier l'effet à appliquer aux zones où le contenu a été déplacé [Moving](../../../aspose.words/revisiontype/). La valeur par défaut est [DoubleUnderline](../../revisiontexteffect/)

```cpp
Aspose::Words::Layout::RevisionTextEffect Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect()
```


## Exemples



Montre comment modifier l'apparence des révisions.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Obtenez l'objet RevisionOptions qui contrôle l'apparence des révisions.
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// Rendez les révisions d'insertion en vert et en italique.
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// Rendez les révisions de suppression en rouge et en gras.
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Le même texte apparaîtra deux fois dans une révision de déplacement :
// une fois au point de départ et une fois à la destination d'arrivée.
// Rendez le texte de la révision déplacée depuis en jaune avec un double barré
// et en bleu doublement souligné dans la révision déplacée vers.
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// Rendez les révisions de format en rouge foncé et en gras.
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Placez une barre épaisse bleu foncé sur le côté gauche de la page à côté des lignes affectées par les révisions.
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// Affichez les marques de révision et le texte original.
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// Obtenez les révisions de déplacement, de suppression, de formatage et les commentaires pour qu'ils apparaissent dans des bulles vertes
// sur le côté droit de la page.
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// Ces fonctionnalités ne s'appliquent qu'aux formats tels que .pdf ou .jpg.
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## Voir aussi

* Enum [RevisionTextEffect](../../revisiontexteffect/)
* Class [RevisionOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
