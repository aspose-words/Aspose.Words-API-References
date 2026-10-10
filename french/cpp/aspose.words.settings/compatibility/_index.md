---
title: "Aspose::Words::Settings::Compatibility enum"
linktitle: "Compatibility"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Settings::Compatibility enum. Spécifie les noms des options de compatibilité en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words.settings/compatibility/
---
## Compatibility enum


Spécifie les noms des options de compatibilité.

```cpp
enum class Compatibility
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| NoTabHangInd | 0 | Pas de retrait suspendu de tabulation. |
| NoSpaceRaiseLower | 1 | Pas de levée/abaissement d'espace. |
| SuppressSpBfAfterPgBrk | 2 | Supprimer l'espace avant le saut de [Paragraph](../../aspose.words/paragraph/). |
| WrapTrailSpaces | 3 | Envelopper les espaces de fin. |
| PrintColBlack | 4 | Imprimer le fond de colonne. |
| NoColumnBalance | 5 | Pas d'équilibrage de colonne. |
| ConvMailMergeEsc | 6 | Convertir les échappements de fusion de courrier. |
| SuppressTopSpacing | 7 | Supprimer l'espacement supérieur. |
| UseSingleBorderforContiguousCells | 8 | Utiliser une seule [Border](../../aspose.words/border/) pour les cellules contiguës. |
| TransparentMetafiles | 9 | Métafichiers transparents. |
| ShowBreaksInFrames | 10 | Afficher les sauts dans les cadres. |
| SwapBordersOddFacingPgs | 11 | Échanger les bordures sur les pages impaires. |
| DoNotLeaveBackslashAlone | 12 | Ne pas laisser la barre oblique inverse seule. |
| DoNotExpandOnShiftReturn | 13 | Ne pas développer sur le retour Maj. |
| UlTrailSpace | 14 | Souligner l'espace de fin. |
| BalanceSingleByteDoubleByteWidth | 15 | Équilibrer les largeurs des caractères simple octet et double octet. |
| SuppressTopSpacingAtTopOfPage | 16 | Supprimer l'espacement de ligne supérieur dans WordPerfect. |
| SpacingInWholePoints | 17 | Espacement en points entiers. |
| PrintBodyTextBeforeHeader | 18 | Imprimer le texte du [Body](../../aspose.words/body/) avant l'en-tête. |
| NoLeading | 19 | Pas d'interligne. |
| SpaceForUL | 20 | Espace pour le soulignement. |
| MWSmallCaps | 21 | Petites majuscules MW. |
| SuppressTopLineSpacingWP | 22 | Supprimer l'espacement de ligne supérieur dans WordPerfect. |
| TruncateFontHeightLikeWP6 | 23 | Tronquer la hauteur de la [Font](../../aspose.words/font/) comme WordPerfect 6. |
| SubFontBySize | 24 | Remplacer la [Font](../../aspose.words/font/) par la taille. |
| LineWrapLikeWord6 | 25 | Retour à la ligne comme Word 6. |
| DoNotSuppressParagraphBorder | 26 | Ne pas supprimer le [Paragraph](../../aspose.words/paragraph/)[Border](../../aspose.words/border/). |
| NoExtraLineSpacing | 27 | Pas d'espacement de ligne supplémentaire. |
| SuppressBottomSpacing | 28 | Supprimer l'espacement inférieur. |
| WPSpaceWidth | 29 | Largeur d'espace WordPerfect. |
| WPJustification | 30 | Justification WordPerfect. |
| UsePrinterMetrics | 31 | Utiliser les métriques de l'imprimante. |
| ShapeLayoutLikeWW8 | 32 | Forme [Layout](../../aspose.words.layout/) comme Word 2000. |
| FootnoteLayoutLikeWW8 | 33 | Note de bas de page [Layout](../../aspose.words.layout/) comme Word 2000. |
| DoNotUseHtmlParagraphAutoSpacing | 34 | Ne pas utiliser l'espacement automatique du [Paragraph](../../aspose.words/paragraph/) HTML. |
| AdjustLineHeightInTable | 35 | Ajuster la hauteur de ligne dans le tableau. |
| ForgetLastTabAlignment | 36 | Oublier l'alignement du dernier onglet. |
| AutoSpaceLikeWord95 | 37 | Espacement automatique comme Word 95. |
| AlignTableRowByRow | 38 | Aligner les lignes du tableau selon la règle. |
| LayoutRawTableWidth | 39 | [Layout](../../aspose.words.layout/) Largeur brute du tableau. |
| LayoutTableRowsApart | 40 | [Layout](../../aspose.words.layout/) Lignes du tableau séparées. |
| UseWord97LineBreakRules | 41 | Utiliser les règles de saut de ligne Word 97. |
| DoNotBreakWrappedTables | 42 | Ne pas casser les [Tables](../../aspose.words.tables/) enveloppées. |
| doNotSnapToGridInCell | 43 | Ne pas aligner sur la grille dans les cellules. |
| SelectFldWithFirstOrLastChar | 44 | Sélectionner le champ avec le premier ou le dernier caractère. |
| ApplyBreakingRules | 45 | Appliquer les règles de césure. |
| DoNotWrapTextWithPunct | 46 | Ne pas renvoyer le texte avec ponctuation. |
| DoNotUseEastAsianBreakRules | 47 | Ne pas utiliser les règles de césure est-asiatiques. |
| UseWord2002TableStyleRules | 48 | Utiliser les règles de tableau Word 2002 [Style](../../aspose.words/style/). |
| GrowAutofit | 49 | Agrandir l'ajustement automatique. |
| UseNormalStyleForList | 50 | Utiliser le [Style](../../aspose.words/style/) Normal pour la liste. |
| DoNotUseIndentAsNumberingTabStop | 51 | Ne pas utiliser l'indentation comme tabulation de numérotation. |
| UseAltKinsokuLineBreakRules | 52 | Utiliser les règles de saut de ligne Alt Kinsoku. |
| AllowSpaceOfSameStyleInTable | 53 | Autoriser l'espace du même [Style](../../aspose.words/style/) dans le tableau. |
| DoNotSuppressIndentation | 54 | Ne pas supprimer l'indentation. |
| DoNotAutofitConstrainedTables | 55 | Ne pas ajuster automatiquement les [Tables](../../aspose.words.tables/) contraintes. |
| AutofitToFirstFixedWidthCell | 56 | Ajuster automatiquement à la première cellule à largeur fixe. |
| UnderlineTabInNumList | 57 | Souligner la tabulation dans la liste numérotée. |
| DisplayHangulFixedWidth | 58 | Afficher la largeur fixe Hangul. |
| SplitPgBreakAndParaMark | 59 | Diviser le saut de page et le marqueur [Paragraph](../../aspose.words/paragraph/). |
| DoNotVertAlignCellWithSp | 60 | Ne pas aligner verticalement la cellule avec l'espacement. |
| DoNotBreakConstrainedForcedTable | 61 | Ne pas rompre les [Tables](../../aspose.words.tables/) contraintes forcées. |
| DoNotVertAlignInTxbx | 62 | Ne pas aligner verticalement dans les zones de texte. |
| UseAnsiKerningPairs | 63 | Utiliser les paires de crénage ANSI. |
| CachedColBalance | 64 | Équilibrage de colonne mis en cache. |
| UseFELayout | 65 | Utiliser le [Layout](../../aspose.words.layout/) d'Extrême-Orient. |
| UICompat97To2003 | 66 | Mode de compatibilité de l'interface utilisateur de Word 97 à Word 2003. |
| OverrideTableStyleFontSizeAndJustification | 67 | Remplacer la taille et la justification du [Style](../../aspose.words/style/)[Font](../../aspose.words/font/) du tableau. |
| DisableOpenTypeFontFormattingFeatures | 68 | Désactiver les fonctionnalités de formatage de la [Font](../../aspose.words/font/) OpenType. |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | 69 | Échanger l'intérieur et l'extérieur pour les retraits miroir et le positionnement relatif. |
| UseWord2010TableStyleRules | 70 | Utiliser les règles du [Style](../../aspose.words/style/) de tableau Word 2010. |

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
