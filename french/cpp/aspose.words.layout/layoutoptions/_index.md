---
title: "Classe Aspose::Words::Layout::LayoutOptions"
linktitle: "LayoutOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Layout::LayoutOptions. Contient les options qui permettent de contrôler le processus de mise en page du document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.layout/layoutoptions/
---
## LayoutOptions class


Contient les options qui permettent de contrôler le processus de mise en page du document. Pour en savoir plus, consultez l'article de documentation [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/).

```cpp
class LayoutOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_Callback](./get_callback/)() const | Obtient l'implémentation de [IPageLayoutCallback](../ipagelayoutcallback/) utilisée par le modèle de mise en page. |
| [get_CommentDisplayMode](./get_commentdisplaymode/)() const | Obtient ou définit la façon dont les commentaires sont rendus. La valeur par défaut est [ShowInBalloons](../commentdisplaymode/). |
| [get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/)() const | Obtient ou définit le mode de comportement pour le calcul des numéros de page lorsqu'une section continue redémarre la numérotation des pages. |
| [get_IgnorePrinterMetrics](./get_ignoreprintermetrics/)() const | Obtient ou définit l'indication de savoir si l'option de compatibilité « Utiliser les métriques de l'imprimante pour mettre en page le document » est ignorée. La valeur par défaut est **true**. |
| [get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/)() const | Obtient ou définit une indication de savoir si les métriques de police originales doivent être utilisées après la substitution de police. La valeur par défaut est **true**. |
| [get_RevisionOptions](./get_revisionoptions/)() const | Obtient les options de révision. |
| [get_ShowHiddenText](./get_showhiddentext/)() const | Obtient ou définit l'indication de savoir si le texte masqué dans le document est rendu. La valeur par défaut est **false**. |
| [get_ShowParagraphMarks](./get_showparagraphmarks/)() const | Obtient ou définit l'indication de savoir si les marques de paragraphe sont rendues. La valeur par défaut est **false**. |
| [get_TextShaperFactory](./get_textshaperfactory/)() const | Obtient l'implémentation de [ITextShaperFactory](../) utilisée pour les fonctionnalités de rendu de typographie avancée. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LayoutOptions](./layoutoptions/)() |  |
| [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::Layout::IPageLayoutCallback\>\&) | Définit l'implémentation de [IPageLayoutCallback](../ipagelayoutcallback/) utilisée par le modèle de mise en page. |
| [set_CommentDisplayMode](./set_commentdisplaymode/)(Aspose::Words::Layout::CommentDisplayMode) | Définisseur pour [Aspose::Words::Layout::LayoutOptions::get_CommentDisplayMode](./get_commentdisplaymode/). |
| [set_ContinuousSectionPageNumberingRestart](./set_continuoussectionpagenumberingrestart/)(Aspose::Words::Layout::ContinuousSectionRestart) | Définisseur pour [Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart](./get_continuoussectionpagenumberingrestart/). |
| [set_IgnorePrinterMetrics](./set_ignoreprintermetrics/)(bool) | Définisseur pour [Aspose::Words::Layout::LayoutOptions::get_IgnorePrinterMetrics](./get_ignoreprintermetrics/). |
| [set_KeepOriginalFontMetrics](./set_keeporiginalfontmetrics/)(bool) | Définisseur pour [Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics](./get_keeporiginalfontmetrics/). |
| [set_ShowHiddenText](./set_showhiddentext/)(bool) | Définisseur pour [Aspose::Words::Layout::LayoutOptions::get_ShowHiddenText](./get_showhiddentext/). |
| [set_ShowParagraphMarks](./set_showparagraphmarks/)(bool) | Définisseur pour [Aspose::Words::Layout::LayoutOptions::get_ShowParagraphMarks](./get_showparagraphmarks/). |
| [set_TextShaperFactory](./set_textshaperfactory/)(const System::SharedPtr\<Aspose::Words::Shaping::ITextShaperFactory\>\&) | Définit l'implémentation de [ITextShaperFactory](../) utilisée pour les fonctionnalités de rendu de typographie avancée. |
| static [Type](./type/)() |  |
## Remarques


Vous ne créez pas d'instances de cette classe directement. Utilisez la propriété [LayoutOptions](../../aspose.words/document/get_layoutoptions/) pour accéder aux options de mise en page de ce document.

Notez qu'après avoir modifié l'une des options présentes dans cette classe, la méthode [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) doit être appelée afin que les options modifiées soient appliquées à la mise en page.

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

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
