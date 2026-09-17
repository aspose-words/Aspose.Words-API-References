---
title: "Aspose::Words::ParagraphFormat classe"
linktitle: "ParagraphFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat classe. Représente l'ensemble du formatage d'un paragraphe. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 49000
url: /fr/cpp/aspose.words/paragraphformat/
---
## ParagraphFormat class


Représente toute la mise en forme d'un paragraphe. Pour en savoir plus, consultez l'article de documentation [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphFormat : public Aspose::Words::IBorderAttrSource,
                        public Aspose::Words::IShadingAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Réinitialise le formatage du paragraphe aux valeurs par défaut. |
| [get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/)() | Obtient ou définit un indicateur indiquant si l'espacement inter-caractères est automatiquement ajusté entre les zones de texte latin et les zones de texte est-asiatique dans le paragraphe actuel. |
| [get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/)() | Obtient ou définit un indicateur indiquant si l'espacement inter-caractères est automatiquement ajusté entre les zones de chiffres et les zones de texte est-asiatique dans le paragraphe actuel. |
| [get_Alignment](./get_alignment/)() | Obtient ou définit l'alignement du texte pour le paragraphe. |
| [get_BaselineAlignment](./get_baselinealignment/)() | Obtient ou définit la position verticale des polices sur une ligne. |
| [get_Bidi](./get_bidi/)() | Obtient ou définit si ce paragraphe est de droite à gauche. |
| [get_Borders](./get_borders/)() | Obtient la collection des bordures du paragraphe. |
| [get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/)() | Obtient ou définit la valeur (en caractères) pour le retrait de première ligne ou le retrait suspendu. Utilisez des valeurs positives pour définir le retrait de première ligne, et des valeurs négatives pour définir le retrait suspendu. |
| [get_CharacterUnitLeftIndent](./get_characterunitleftindent/)() | Obtient ou définit la valeur du retrait gauche (en caractères) pour les paragraphes spécifiés. |
| [get_CharacterUnitRightIndent](./get_characterunitrightindent/)() | Obtient ou définit la valeur du retrait droit (en caractères) pour les paragraphes spécifiés. |
| [get_DropCapPosition](./get_dropcapposition/)() | Obtient ou définit la position du texte en lettrine. |
| [get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/)() | Obtient ou définit un indicateur indiquant si les règles de césure est-asiatiques sont appliquées au paragraphe actuel. |
| [get_FirstLineIndent](./get_firstlineindent/)() | Obtient ou définit la valeur (en points) pour un retrait de première ligne ou un retrait suspendu. Utilisez des valeurs positives pour définir le retrait de première ligne, et des valeurs négatives pour définir le retrait suspendu. |
| [get_HangingPunctuation](./get_hangingpunctuation/)() | Obtient ou définit un indicateur indiquant si la ponctuation suspendue est activée pour le paragraphe actuel. |
| [get_IsHeading](./get_isheading/)() | Vrai lorsque le style de paragraphe est l'un des styles de titre intégrés. |
| [get_IsListItem](./get_islistitem/)() | Vrai lorsque le paragraphe est un élément d'une liste à puces ou numérotée. |
| [get_KeepTogether](./get_keeptogether/)() | Vrai si toutes les lignes du paragraphe doivent rester sur la même page. |
| [get_KeepWithNext](./get_keepwithnext/)() | Vrai si le paragraphe doit rester sur la même page que le paragraphe qui le suit. |
| [get_LeftIndent](./get_leftindent/)() | Obtient ou définit la valeur (en points) qui représente le retrait gauche pour le paragraphe. |
| [get_LineSpacing](./get_linespacing/)() | Obtient ou définit l'espacement des lignes (en points) pour le paragraphe. |
| [get_LineSpacingRule](./get_linespacingrule/)() | Obtient ou définit l'espacement des lignes pour le paragraphe. |
| [get_LinesToDrop](./get_linestodrop/)() | Obtient ou définit le nombre de lignes du texte du paragraphe utilisées pour calculer la hauteur de la lettrine. |
| [get_LineUnitAfter](./get_lineunitafter/)() | Obtient ou définit la quantité d'espacement (en lignes de grille) après les paragraphes. |
| [get_LineUnitBefore](./get_lineunitbefore/)() | Obtient ou définit la quantité d'espacement (en lignes de grille) avant les paragraphes. |
| [get_MirrorIndents](./get_mirrorindents/)() | Obtient ou définit un indicateur indiquant si les retraits gauche et droit ont la même largeur. |
| [get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/)() | Lorsque **true**, [SpaceBefore](./get_spacebefore/) et [SpaceAfter](./get_spaceafter/) seront ignorés entre les paragraphes du même style. |
| [get_OutlineLevel](./get_outlinelevel/)() | Spécifie le niveau de plan du paragraphe dans le document. |
| [get_PageBreakBefore](./get_pagebreakbefore/)() | Vrai si un saut de page est forcé avant le paragraphe. |
| [get_RightIndent](./get_rightindent/)() | Obtient ou définit la valeur (en points) qui représente le retrait droit du paragraphe. |
| [get_Shading](./get_shading/)() | Renvoie un objet [Shading](../shading/) qui fait référence au format d’ombrage du paragraphe. |
| [get_SnapToGrid](./get_snaptogrid/)() | Spécifie si le paragraphe actuel doit utiliser les paramètres de lignes de grille du document par page lors de la mise en page du contenu du paragraphe. |
| [get_SpaceAfter](./get_spaceafter/)() | Obtient ou définit la quantité d’espacement (en points) après le paragraphe. |
| [get_SpaceAfterAuto](./get_spaceafterauto/)() | Vrai si la quantité d’espacement après le paragraphe est définie automatiquement. |
| [get_SpaceBefore](./get_spacebefore/)() | Obtient ou définit la quantité d’espacement (en points) avant le paragraphe. |
| [get_SpaceBeforeAuto](./get_spacebeforeauto/)() | Vrai si la quantité d’espacement avant le paragraphe est définie automatiquement. |
| [get_Style](./get_style/)() | Obtient ou définit le style de paragraphe appliqué à ce formatage. |
| [get_StyleIdentifier](./get_styleidentifier/)() | Obtient ou définit l’identifiant de style indépendant de la locale du style de paragraphe appliqué à ce formatage. |
| [get_StyleName](./get_stylename/)() | Obtient ou définit le nom du style de paragraphe appliqué à ce formatage. |
| [get_SuppressAutoHyphens](./get_suppressautohyphens/)() | Spécifie si le paragraphe actuel doit être exempté de toute césure appliquée dans les paramètres du document. |
| [get_SuppressLineNumbers](./get_suppresslinenumbers/)() | Spécifie si les lignes du paragraphe actuel doivent être exemptées de la numérotation des lignes appliquée dans la section parente. |
| [get_TabStops](./get_tabstops/)() | Obtient la collection d’arrêts de tabulation personnalisés définis pour cet objet. |
| [get_WidowControl](./get_widowcontrol/)() | Vrai si les première et dernière lignes du paragraphe doivent rester sur la même page que le reste du paragraphe. |
| [get_WordWrap](./get_wordwrap/)() | Si cette propriété est **false**, le texte latin au milieu d’un mot peut être renvoyé à la ligne pour le paragraphe actuel. Sinon, le texte latin est renvoyé à la ligne par mots entiers. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AddSpaceBetweenFarEastAndAlpha](./set_addspacebetweenfareastandalpha/)(bool) | Définisseur pour [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha](./get_addspacebetweenfareastandalpha/). |
| [set_AddSpaceBetweenFarEastAndDigit](./set_addspacebetweenfareastanddigit/)(bool) | Définisseur pour [Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndDigit](./get_addspacebetweenfareastanddigit/). |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Définisseur pour [Aspose::Words::ParagraphFormat::get_Alignment](./get_alignment/). |
| [set_BaselineAlignment](./set_baselinealignment/)(Aspose::Words::BaselineAlignment) | Définisseur pour [Aspose::Words::ParagraphFormat::get_BaselineAlignment](./get_baselinealignment/). |
| [set_Bidi](./set_bidi/)(bool) | Définisseur pour [Aspose::Words::ParagraphFormat::get_Bidi](./get_bidi/). |
| [set_CharacterUnitFirstLineIndent](./set_characterunitfirstlineindent/)(double) | Définisseur pour [Aspose::Words::ParagraphFormat::get_CharacterUnitFirstLineIndent](./get_characterunitfirstlineindent/). |
| [set_CharacterUnitLeftIndent](./set_characterunitleftindent/)(double) | Définisseur pour [Aspose::Words::ParagraphFormat::get_CharacterUnitLeftIndent](./get_characterunitleftindent/). |
| [set_CharacterUnitRightIndent](./set_characterunitrightindent/)(double) | Définisseur pour [Aspose::Words::ParagraphFormat::get_CharacterUnitRightIndent](./get_characterunitrightindent/). |
| [set_DropCapPosition](./set_dropcapposition/)(Aspose::Words::DropCapPosition) | Définisseur pour [Aspose::Words::ParagraphFormat::get_DropCapPosition](./get_dropcapposition/). |
| [set_FarEastLineBreakControl](./set_fareastlinebreakcontrol/)(bool) | Définisseur pour [Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl](./get_fareastlinebreakcontrol/). |
| [set_FirstLineIndent](./set_firstlineindent/)(double) | Définisseur de [Aspose::Words::ParagraphFormat::get_FirstLineIndent](./get_firstlineindent/). |
| [set_HangingPunctuation](./set_hangingpunctuation/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_HangingPunctuation](./get_hangingpunctuation/). |
| [set_KeepTogether](./set_keeptogether/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_KeepTogether](./get_keeptogether/). |
| [set_KeepWithNext](./set_keepwithnext/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_KeepWithNext](./get_keepwithnext/). |
| [set_LeftIndent](./set_leftindent/)(double) | Définisseur de [Aspose::Words::ParagraphFormat::get_LeftIndent](./get_leftindent/). |
| [set_LineSpacing](./set_linespacing/)(double) | Définisseur de [Aspose::Words::ParagraphFormat::get_LineSpacing](./get_linespacing/). |
| [set_LineSpacingRule](./set_linespacingrule/)(Aspose::Words::LineSpacingRule) | Définisseur de [Aspose::Words::ParagraphFormat::get_LineSpacingRule](./get_linespacingrule/). |
| [set_LinesToDrop](./set_linestodrop/)(int32_t) | Définisseur de [Aspose::Words::ParagraphFormat::get_LinesToDrop](./get_linestodrop/). |
| [set_LineUnitAfter](./set_lineunitafter/)(double) | Définisseur de [Aspose::Words::ParagraphFormat::get_LineUnitAfter](./get_lineunitafter/). |
| [set_LineUnitBefore](./set_lineunitbefore/)(double) | Définisseur de [Aspose::Words::ParagraphFormat::get_LineUnitBefore](./get_lineunitbefore/). |
| [set_MirrorIndents](./set_mirrorindents/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_MirrorIndents](./get_mirrorindents/). |
| [set_NoSpaceBetweenParagraphsOfSameStyle](./set_nospacebetweenparagraphsofsamestyle/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle](./get_nospacebetweenparagraphsofsamestyle/). |
| [set_OutlineLevel](./set_outlinelevel/)(Aspose::Words::OutlineLevel) | Définisseur de [Aspose::Words::ParagraphFormat::get_OutlineLevel](./get_outlinelevel/). |
| [set_PageBreakBefore](./set_pagebreakbefore/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_PageBreakBefore](./get_pagebreakbefore/). |
| [set_RightIndent](./set_rightindent/)(double) | Définisseur de [Aspose::Words::ParagraphFormat::get_RightIndent](./get_rightindent/). |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_SnapToGrid](./get_snaptogrid/). |
| [set_SpaceAfter](./set_spaceafter/)(double) | Définisseur de [Aspose::Words::ParagraphFormat::get_SpaceAfter](./get_spaceafter/). |
| [set_SpaceAfterAuto](./set_spaceafterauto/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_SpaceAfterAuto](./get_spaceafterauto/). |
| [set_SpaceBefore](./set_spacebefore/)(double) | Définisseur de [Aspose::Words::ParagraphFormat::get_SpaceBefore](./get_spacebefore/). |
| [set_SpaceBeforeAuto](./set_spacebeforeauto/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_SpaceBeforeAuto](./get_spacebeforeauto/). |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Définisseur de [Aspose::Words::ParagraphFormat::get_Style](./get_style/). |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | Définisseur de [Aspose::Words::ParagraphFormat::get_StyleIdentifier](./get_styleidentifier/). |
| [set_StyleName](./set_stylename/)(const System::String\&) | Définisseur de [Aspose::Words::ParagraphFormat::get_StyleName](./get_stylename/). |
| [set_SuppressAutoHyphens](./set_suppressautohyphens/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens](./get_suppressautohyphens/). |
| [set_SuppressLineNumbers](./set_suppresslinenumbers/)(bool) | Définisseur de [Aspose::Words::ParagraphFormat::get_SuppressLineNumbers](./get_suppresslinenumbers/). |
| [set_WidowControl](./set_widowcontrol/)(bool) | Définisseur pour [Aspose::Words::ParagraphFormat::get_WidowControl](./get_widowcontrol/). |
| [set_WordWrap](./set_wordwrap/)(bool) | Définisseur pour [Aspose::Words::ParagraphFormat::get_WordWrap](./get_wordwrap/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment construire un document Aspose.Words à la main.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vierge contient une section, un corps et un paragraphe.
// Appelez la méthode "RemoveAllChildren" pour supprimer tous ces nœuds,
// et obtenez un nœud de document sans enfants.
doc->RemoveAllChildren();

// Ce document n’a maintenant aucun nœud enfant composite auquel nous puissions ajouter du contenu.
// Si nous souhaitons le modifier, nous devrons reconstituer sa collection de nœuds.
// Tout d’abord, créez une nouvelle section, puis ajoutez-la en tant qu’enfant au nœud racine du document.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Définissez quelques propriétés de mise en page pour la section.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Une section nécessite un corps, qui contiendra et affichera tout son contenu
// sur la page entre l’en-tête et le pied-de-page de la section.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Créez un paragraphe, définissez quelques propriétés de mise en forme, puis ajoutez‑le en tant qu’enfant au corps.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Enfin, ajoutez du contenu au document. Créez un run,
// définissez son apparence et son contenu, puis ajoutez‑le en tant qu’enfant au paragraphe.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
