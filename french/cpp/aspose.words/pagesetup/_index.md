---
title: "Aspose::Words::PageSetup class"
linktitle: "PageSetup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::PageSetup class. Représente les propriétés de configuration de page d'une section. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 46000
url: /fr/cpp/aspose.words/pagesetup/
---
## PageSetup class


Représente les propriétés de configuration de page d'une section. Pour en savoir plus, consultez l'article de documentation [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class PageSetup : public Aspose::Words::IBorderAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Réinitialise la configuration de page à la taille de papier, aux marges et à l'orientation par défaut. |
| [get_Bidi](./get_bidi/)() | Spécifie que cette section contient du texte bidirectionnel (scripts complexes). |
| [get_BorderAlwaysInFront](./get_borderalwaysinfront/)() | Spécifie où la bordure de page est positionnée par rapport aux textes et objets qui s'intersectent. |
| [get_BorderAppliesTo](./get_borderappliesto/)() | Spécifie sur quelles pages la bordure de page est imprimée. |
| [get_BorderDistanceFrom](./get_borderdistancefrom/)() | Obtient ou définit une valeur indiquant si la bordure de page spécifiée est mesurée depuis le bord de la page ou depuis le texte qu'elle entoure. |
| [get_Borders](./get_borders/)() | Obtient une collection des bordures de page. |
| [get_BorderSurroundsFooter](./get_bordersurroundsfooter/)() | Spécifie si la bordure de page inclut ou exclut le pied de page. |
| [get_BorderSurroundsHeader](./get_bordersurroundsheader/)() | Spécifie si la bordure de page inclut ou exclut l'en-tête. |
| [get_BottomMargin](./get_bottommargin/)() | Renvoie ou définit la distance (en points) entre le bord inférieur de la page et la limite inférieure du texte principal. |
| [get_ChapterPageSeparator](./get_chapterpageseparator/)() | Obtient ou définit le caractère séparateur qui apparaît entre le numéro du chapitre et le numéro de page. |
| [get_CharactersPerLine](./get_charactersperline/)() | Obtient ou définit le nombre de caractères par ligne dans la grille du document. |
| [get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/)() | Vrai si un en-tête ou pied de page différent est utilisé sur la première page. |
| [get_EndnoteOptions](./get_endnoteoptions/)() | Fournit des options qui contrôlent la numérotation et le positionnement des notes de fin dans cette section. |
| [get_FirstPageTray](./get_firstpagetray/)() | Obtient le bac (trémie) de papier à utiliser pour la première page d’une section. La valeur dépend de l’implémentation (imprimante). |
| [get_FooterDistance](./get_footerdistance/)() | Renvoie ou définit la distance (en points) entre le pied de page et le bas de la page. |
| [get_FootnoteOptions](./get_footnoteoptions/)() | Fournit des options qui contrôlent la numérotation et le positionnement des notes de bas de page dans cette section. |
| [get_Gutter](./get_gutter/)() | Obtient ou définit la quantité d’espace supplémentaire ajoutée à la marge pour la reliure du document. |
| [get_HeaderDistance](./get_headerdistance/)() | Renvoie ou définit la distance (en points) entre l’en-tête et le haut de la page. |
| [get_HeadingLevelForChapter](./get_headinglevelforchapter/)() | Obtient ou définit le style de niveau de titre appliqué aux titres de chapitres dans le document. |
| [get_LayoutMode](./get_layoutmode/)() | Obtient ou définit le mode de mise en page de cette section. |
| [get_LeftMargin](./get_leftmargin/)() | Renvoie ou définit la distance (en points) entre le bord gauche de la page et la limite gauche du texte principal. |
| [get_LineNumberCountBy](./get_linenumbercountby/)() | Renvoie ou définit l’incrément numérique pour les numéros de ligne. |
| [get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/)() | Obtient ou définit la distance entre le bord droit des numéros de ligne et le bord gauche du document. |
| [get_LineNumberRestartMode](./get_linenumberrestartmode/)() | Obtient ou définit la façon dont la numérotation des lignes s’exécute, c’est‑à‑dire si elle recommence au début d’une nouvelle page ou section ou si elle continue de façon continue. |
| [get_LinesPerPage](./get_linesperpage/)() | Obtient ou définit le nombre de lignes par page dans la grille du document. |
| [get_LineStartingNumber](./get_linestartingnumber/)() | Obtient ou définit le numéro de ligne de départ. |
| [get_Margins](./get_margins/)() | Renvoie ou définit les [Margins](../margins/) prédéfinies de la page. |
| [get_MultiplePages](./get_multiplepages/)() const | Pour les documents à plusieurs pages, obtient ou définit comment un document est imprimé ou rendu afin qu’il puisse être relié sous forme de livret. |
| [get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/)() const | Vrai si le document possède des en-têtes et pieds de page différents pour les pages impaires et paires. |
| [get_Orientation](./get_orientation/)() | Renvoie ou définit l’orientation de la page. |
| [get_OtherPagesTray](./get_otherpagestray/)() | Obtient le bac (trémie) de papier à utiliser pour toutes les pages sauf la première d’une section. La valeur dépend de l’implémentation (imprimante). |
| [get_PageHeight](./get_pageheight/)() | Renvoie ou définit la hauteur de la page en points. |
| [get_PageNumberStyle](./get_pagenumberstyle/)() | Obtient ou définit le format du numéro de page. |
| [get_PageStartingNumber](./get_pagestartingnumber/)() | Obtient ou définit le numéro de page de départ de la section. |
| [get_PageWidth](./get_pagewidth/)() | Renvoie ou définit la largeur de la page en points. |
| [get_PaperSize](./get_papersize/)() | Renvoie ou définit la taille du papier. |
| [get_RestartPageNumbering](./get_restartpagenumbering/)() | Vrai si la numérotation des pages redémarre au début de la section. |
| [get_RightMargin](./get_rightmargin/)() | Renvoie ou définit la distance (en points) entre le bord droit de la page et la limite droite du texte principal. |
| [get_RtlGutter](./get_rtlgutter/)() | Obtient ou définit si Microsoft Word utilise des gouttières pour la section en fonction d’une langue de droite à gauche ou de gauche à droite. |
| [get_SectionStart](./get_sectionstart/)() | Renvoie ou définit le type de saut de section pour l’objet spécifié. |
| [get_SheetsPerBooklet](./get_sheetsperbooklet/)() const | Renvoie ou définit le nombre de pages à inclure dans chaque livret. |
| [get_SuppressEndnotes](./get_suppressendnotes/)() | Vrai si les notes de fin sont imprimées à la fin de la section suivante qui ne supprime pas les notes de fin. Les notes de fin supprimées sont imprimées avant les notes de fin dans cette section. |
| [get_TextColumns](./get_textcolumns/)() | Renvoie une collection qui représente l’ensemble des colonnes de texte. |
| [get_TextOrientation](./get_textorientation/)() | Permet de spécifier [TextOrientation](./get_textorientation/) pour toute la page. La valeur par défaut est [Horizontal](../textorientation/) |
| [get_TopMargin](./get_topmargin/)() | Renvoie ou définit la distance (en points) entre le bord supérieur de la page et la limite supérieure du texte principal. |
| [get_VerticalAlignment](./get_verticalalignment/)() | Renvoie ou définit l’alignement vertical du texte sur chaque page d’un document ou d’une section. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bidi](./set_bidi/)(bool) | Mutateur pour [Aspose::Words::PageSetup::get_Bidi](./get_bidi/). |
| [set_BorderAlwaysInFront](./set_borderalwaysinfront/)(bool) | Mutateur pour [Aspose::Words::PageSetup::get_BorderAlwaysInFront](./get_borderalwaysinfront/). |
| [set_BorderAppliesTo](./set_borderappliesto/)(Aspose::Words::PageBorderAppliesTo) | Mutateur pour [Aspose::Words::PageSetup::get_BorderAppliesTo](./get_borderappliesto/). |
| [set_BorderDistanceFrom](./set_borderdistancefrom/)(Aspose::Words::PageBorderDistanceFrom) | Mutateur pour [Aspose::Words::PageSetup::get_BorderDistanceFrom](./get_borderdistancefrom/). |
| [set_BorderSurroundsFooter](./set_bordersurroundsfooter/)(bool) | Mutateur pour [Aspose::Words::PageSetup::get_BorderSurroundsFooter](./get_bordersurroundsfooter/). |
| [set_BorderSurroundsHeader](./set_bordersurroundsheader/)(bool) | Mutateur pour [Aspose::Words::PageSetup::get_BorderSurroundsHeader](./get_bordersurroundsheader/). |
| [set_BottomMargin](./set_bottommargin/)(double) | Mutateur pour [Aspose::Words::PageSetup::get_BottomMargin](./get_bottommargin/). |
| [set_ChapterPageSeparator](./set_chapterpageseparator/)(Aspose::Words::ChapterPageSeparator) | Mutateur pour [Aspose::Words::PageSetup::get_ChapterPageSeparator](./get_chapterpageseparator/). |
| [set_CharactersPerLine](./set_charactersperline/)(int32_t) | Mutateur pour [Aspose::Words::PageSetup::get_CharactersPerLine](./get_charactersperline/). |
| [set_DifferentFirstPageHeaderFooter](./set_differentfirstpageheaderfooter/)(bool) | Mutateur pour [Aspose::Words::PageSetup::get_DifferentFirstPageHeaderFooter](./get_differentfirstpageheaderfooter/). |
| [set_FirstPageTray](./set_firstpagetray/)(int32_t) | Définit le bac à papier à utiliser pour la première page d’une section. La valeur dépend de l’implémentation (imprimante). |
| [set_FooterDistance](./set_footerdistance/)(double) | Mutateur pour [Aspose::Words::PageSetup::get_FooterDistance](./get_footerdistance/). |
| [set_Gutter](./set_gutter/)(double) | Mutateur pour [Aspose::Words::PageSetup::get_Gutter](./get_gutter/). |
| [set_HeaderDistance](./set_headerdistance/)(double) | Définisseur pour [Aspose::Words::PageSetup::get_HeaderDistance](./get_headerdistance/). |
| [set_HeadingLevelForChapter](./set_headinglevelforchapter/)(int32_t) | Définisseur pour [Aspose::Words::PageSetup::get_HeadingLevelForChapter](./get_headinglevelforchapter/). |
| [set_LayoutMode](./set_layoutmode/)(Aspose::Words::SectionLayoutMode) | Définisseur pour [Aspose::Words::PageSetup::get_LayoutMode](./get_layoutmode/). |
| [set_LeftMargin](./set_leftmargin/)(double) | Définisseur pour [Aspose::Words::PageSetup::get_LeftMargin](./get_leftmargin/). |
| [set_LineNumberCountBy](./set_linenumbercountby/)(int32_t) | Définisseur pour [Aspose::Words::PageSetup::get_LineNumberCountBy](./get_linenumbercountby/). |
| [set_LineNumberDistanceFromText](./set_linenumberdistancefromtext/)(double) | Définisseur pour [Aspose::Words::PageSetup::get_LineNumberDistanceFromText](./get_linenumberdistancefromtext/). |
| [set_LineNumberRestartMode](./set_linenumberrestartmode/)(Aspose::Words::LineNumberRestartMode) | Définisseur pour [Aspose::Words::PageSetup::get_LineNumberRestartMode](./get_linenumberrestartmode/). |
| [set_LinesPerPage](./set_linesperpage/)(int32_t) | Définisseur pour [Aspose::Words::PageSetup::get_LinesPerPage](./get_linesperpage/). |
| [set_LineStartingNumber](./set_linestartingnumber/)(int32_t) | Définisseur pour [Aspose::Words::PageSetup::get_LineStartingNumber](./get_linestartingnumber/). |
| [set_Margins](./set_margins/)(Aspose::Words::Margins) | Définisseur pour [Aspose::Words::PageSetup::get_Margins](./get_margins/). |
| [set_MultiplePages](./set_multiplepages/)(Aspose::Words::Settings::MultiplePagesType) | Définisseur pour [Aspose::Words::PageSetup::get_MultiplePages](./get_multiplepages/). |
| [set_OddAndEvenPagesHeaderFooter](./set_oddandevenpagesheaderfooter/)(bool) | Définisseur pour [Aspose::Words::PageSetup::get_OddAndEvenPagesHeaderFooter](./get_oddandevenpagesheaderfooter/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Orientation) | Définisseur pour [Aspose::Words::PageSetup::get_Orientation](./get_orientation/). |
| [set_OtherPagesTray](./set_otherpagestray/)(int32_t) | Définit le bac à papier (trémie) à utiliser pour toutes les pages sauf la première d’une section. La valeur dépend de l’implémentation (imprimante). |
| [set_PageHeight](./set_pageheight/)(double) | Définisseur pour [Aspose::Words::PageSetup::get_PageHeight](./get_pageheight/). |
| [set_PageNumberStyle](./set_pagenumberstyle/)(Aspose::Words::NumberStyle) | Définisseur pour [Aspose::Words::PageSetup::get_PageNumberStyle](./get_pagenumberstyle/). |
| [set_PageStartingNumber](./set_pagestartingnumber/)(int32_t) | Définisseur pour [Aspose::Words::PageSetup::get_PageStartingNumber](./get_pagestartingnumber/). |
| [set_PageWidth](./set_pagewidth/)(double) | Définisseur pour [Aspose::Words::PageSetup::get_PageWidth](./get_pagewidth/). |
| [set_PaperSize](./set_papersize/)(Aspose::Words::PaperSize) | Définisseur pour [Aspose::Words::PageSetup::get_PaperSize](./get_papersize/). |
| [set_RestartPageNumbering](./set_restartpagenumbering/)(bool) | Définisseur pour [Aspose::Words::PageSetup::get_RestartPageNumbering](./get_restartpagenumbering/). |
| [set_RightMargin](./set_rightmargin/)(double) | Définisseur pour [Aspose::Words::PageSetup::get_RightMargin](./get_rightmargin/). |
| [set_RtlGutter](./set_rtlgutter/)(bool) | Définisseur pour [Aspose::Words::PageSetup::get_RtlGutter](./get_rtlgutter/). |
| [set_SectionStart](./set_sectionstart/)(Aspose::Words::SectionStart) | Définisseur pour [Aspose::Words::PageSetup::get_SectionStart](./get_sectionstart/). |
| [set_SheetsPerBooklet](./set_sheetsperbooklet/)(int32_t) | Définisseur pour [Aspose::Words::PageSetup::get_SheetsPerBooklet](./get_sheetsperbooklet/). |
| [set_SuppressEndnotes](./set_suppressendnotes/)(bool) | Vrai si les notes de fin sont imprimées à la fin de la section suivante qui ne supprime pas les notes de fin. Les notes de fin supprimées sont imprimées avant les notes de fin dans cette section. |
| [set_TextOrientation](./set_textorientation/)(Aspose::Words::TextOrientation) | Définisseur pour [Aspose::Words::PageSetup::get_TextOrientation](./get_textorientation/). |
| [set_TopMargin](./set_topmargin/)(double) | Définisseur pour [Aspose::Words::PageSetup::get_TopMargin](./get_topmargin/). |
| [set_VerticalAlignment](./set_verticalalignment/)(Aspose::Words::PageVerticalAlignment) | Définisseur pour [Aspose::Words::PageSetup::get_VerticalAlignment](./get_verticalalignment/). |
| static [Type](./type/)() |  |
## Remarques


[PageSetup](./) object contains all the page setup attributes of a section (left margin, bottom margin, paper size, and so on) as properties.

## Exemples



Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifiez les propriétés de mise en page pour la section actuelle du constructeur et ajoutez du texte.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Si nous commençons une nouvelle section en utilisant un constructeur de document,
// elle héritera des propriétés de mise en page actuelles du constructeur.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Nous pouvons rétablir ses propriétés de mise en page à leurs valeurs par défaut en utilisant la méthode "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
