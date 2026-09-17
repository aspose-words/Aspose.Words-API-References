---
title: "classe Aspose::Words::Layout::RevisionOptions"
linktitle: "RevisionOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::Layout::RevisionOptions. Permet de contrôler la façon dont les révisions de document sont gérées pendant le processus de mise en page. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.layout/revisionoptions/
---
## RevisionOptions class


Permet de contrôler la façon dont les révisions du document sont gérées pendant le processus de mise en page. Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class RevisionOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CommentColor](./get_commentcolor/)() const | Permet de spécifier la couleur à utiliser pour les commentaires. La valeur par défaut est [Red](../revisioncolor/). |
| [get_DeleteCellColor](./get_deletecellcolor/)() | Permet de spécifier la couleur à utiliser pour les cellules supprimées [Deletion](../../aspose.words/revisiontype/). La valeur par défaut est [Pink](../revisioncolor/). |
| [get_DeletedTextColor](./get_deletedtextcolor/)() | Permet de spécifier la couleur à utiliser pour le contenu supprimé [Deletion](../../aspose.words/revisiontype/). La valeur par défaut est [ByAuthor](../revisioncolor/). |
| [get_DeletedTextEffect](./get_deletedtexteffect/)() | Permet de spécifier l'effet à appliquer au contenu supprimé [Deletion](../../aspose.words/revisiontype/). La valeur par défaut est [StrikeThrough](../revisiontexteffect/) |
| [get_InsertCellColor](./get_insertcellcolor/)() | Permet de spécifier la couleur à utiliser pour les cellules insérées [Insertion](../../aspose.words/revisiontype/). La valeur par défaut est [Blue](../revisioncolor/). |
| [get_InsertedTextColor](./get_insertedtextcolor/)() | Permet de spécifier la couleur à utiliser pour le contenu inséré [Insertion](../../aspose.words/revisiontype/). La valeur par défaut est [ByAuthor](../revisioncolor/). |
| [get_InsertedTextEffect](./get_insertedtexteffect/)() | Permet de spécifier l'effet à appliquer au contenu inséré [Insertion](../../aspose.words/revisiontype/). La valeur par défaut est [Underline](../revisiontexteffect/). |
| [get_MeasurementUnit](./get_measurementunit/)() const | Permet de spécifier les unités de mesure pour les commentaires de révision. La valeur par défaut est [Centimeters](../../aspose.words/measurementunits/) |
| [get_MovedFromTextColor](./get_movedfromtextcolor/)() | Permet de spécifier la couleur à utiliser pour les zones d'où le contenu a été déplacé [Moving](../../aspose.words/revisiontype/). La valeur par défaut est [ByAuthor](../revisioncolor/). |
| [get_MovedFromTextEffect](./get_movedfromtexteffect/)() | Permet de spécifier l'effet à appliquer aux zones d'où le contenu a été déplacé [Moving](../../aspose.words/revisiontype/). La valeur par défaut est [DoubleStrikeThrough](../revisiontexteffect/) |
| [get_MovedToTextColor](./get_movedtotextcolor/)() | Permet de spécifier la couleur à utiliser pour les zones vers lesquelles le contenu a été déplacé [Moving](../../aspose.words/revisiontype/). La valeur par défaut est [ByAuthor](../revisioncolor/). |
| [get_MovedToTextEffect](./get_movedtotexteffect/)() | Permet de spécifier l'effet à appliquer aux zones vers lesquelles le contenu a été déplacé [Moving](../../aspose.words/revisiontype/). La valeur par défaut est [DoubleUnderline](../revisiontexteffect/) |
| [get_RevisedPropertiesColor](./get_revisedpropertiescolor/)() | Permet de spécifier la couleur à utiliser pour le contenu avec des modifications de propriétés de formatage [FormatChange](../../aspose.words/revisiontype/) La valeur par défaut est [NoHighlight](../revisioncolor/). |
| [get_RevisedPropertiesEffect](./get_revisedpropertieseffect/)() | Permet de spécifier l'effet pour les zones de contenu avec des modifications de propriétés de formatage [FormatChange](../../aspose.words/revisiontype/) La valeur par défaut est [None](../revisiontexteffect/) |
| [get_RevisionBarsColor](./get_revisionbarscolor/)() const | Permet de spécifier la couleur à utiliser pour les barres latérales qui identifient les lignes de document contenant des informations révisées. La valeur par défaut est [Red](../revisioncolor/). |
| [get_RevisionBarsPosition](./get_revisionbarsposition/)() const | Obtient ou définit la position de rendu des barres de révision. La valeur par défaut est [Outside](../../aspose.words.drawing/horizontalalignment/). |
| [get_RevisionBarsWidth](./get_revisionbarswidth/)() const | Obtient ou définit la largeur des barres de révision, en points. |
| [get_ShowInBalloons](./get_showinballoons/)() const | Permet de spécifier si les révisions sont rendues dans les bulles. La valeur par défaut est [None](../showinballoons/). |
| [get_ShowOriginalRevision](./get_showoriginalrevision/)() const | Permet de spécifier si le texte original doit être affiché à la place du texte révisé. La valeur par défaut est **false**. |
| [get_ShowRevisionBars](./get_showrevisionbars/)() const | Permet de spécifier si les barres de révision doivent être rendues près des lignes contenant du contenu révisé. La valeur par défaut est **true**. |
| [get_ShowRevisionMarks](./get_showrevisionmarks/)() const | Permet de spécifier si le texte de révision doit être marqué avec une mise en forme spéciale. La valeur par défaut est **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CommentColor](./set_commentcolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur pour [Aspose::Words::Layout::RevisionOptions::get_CommentColor](./get_commentcolor/). |
| [set_DeleteCellColor](./set_deletecellcolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_DeleteCellColor](./get_deletecellcolor/). |
| [set_DeletedTextColor](./set_deletedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_DeletedTextColor](./get_deletedtextcolor/). |
| [set_DeletedTextEffect](./set_deletedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_DeletedTextEffect](./get_deletedtexteffect/). |
| [set_InsertCellColor](./set_insertcellcolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_InsertCellColor](./get_insertcellcolor/). |
| [set_InsertedTextColor](./set_insertedtextcolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_InsertedTextColor](./get_insertedtextcolor/). |
| [set_InsertedTextEffect](./set_insertedtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_InsertedTextEffect](./get_insertedtexteffect/). |
| [set_MeasurementUnit](./set_measurementunit/)(Aspose::Words::MeasurementUnits) | Permet de spécifier les unités de mesure pour les commentaires de révision. La valeur par défaut est [Centimeters](../../aspose.words/measurementunits/) |
| [set_MovedFromTextColor](./set_movedfromtextcolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextColor](./get_movedfromtextcolor/). |
| [set_MovedFromTextEffect](./set_movedfromtexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_MovedFromTextEffect](./get_movedfromtexteffect/). |
| [set_MovedToTextColor](./set_movedtotextcolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_MovedToTextColor](./get_movedtotextcolor/). |
| [set_MovedToTextEffect](./set_movedtotexteffect/)(Aspose::Words::Layout::RevisionTextEffect) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_MovedToTextEffect](./get_movedtotexteffect/). |
| [set_RevisedPropertiesColor](./set_revisedpropertiescolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesColor](./get_revisedpropertiescolor/). |
| [set_RevisedPropertiesEffect](./set_revisedpropertieseffect/)(Aspose::Words::Layout::RevisionTextEffect) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_RevisedPropertiesEffect](./get_revisedpropertieseffect/). |
| [set_RevisionBarsColor](./set_revisionbarscolor/)(Aspose::Words::Layout::RevisionColor) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsColor](./get_revisionbarscolor/). |
| [set_RevisionBarsPosition](./set_revisionbarsposition/)(Aspose::Words::Drawing::HorizontalAlignment) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsPosition](./get_revisionbarsposition/). |
| [set_RevisionBarsWidth](./set_revisionbarswidth/)(float) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_RevisionBarsWidth](./get_revisionbarswidth/). |
| [set_ShowInBalloons](./set_showinballoons/)(Aspose::Words::Layout::ShowInBalloons) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_ShowInBalloons](./get_showinballoons/). |
| [set_ShowOriginalRevision](./set_showoriginalrevision/)(bool) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_ShowOriginalRevision](./get_showoriginalrevision/). |
| [set_ShowRevisionBars](./set_showrevisionbars/)(bool) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionBars](./get_showrevisionbars/). |
| [set_ShowRevisionMarks](./set_showrevisionmarks/)(bool) | Définisseur de [Aspose::Words::Layout::RevisionOptions::get_ShowRevisionMarks](./get_showrevisionmarks/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
