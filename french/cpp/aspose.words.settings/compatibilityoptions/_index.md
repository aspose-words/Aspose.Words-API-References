---
title: "Classe Aspose::Words::Settings::CompatibilityOptions"
linktitle: "CompatibilityOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Settings::CompatibilityOptions. Contient les options de compatibilité (c’est‑à‑dire les préférences utilisateur saisies dans l’onglet Compatibilité de la boîte de dialogue Options de Microsoft Word). Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.settings/compatibilityoptions/
---
## CompatibilityOptions class


Contient des options de compatibilité (c'est‑à‑dire les préférences utilisateur saisies dans l'onglet **Compatibility** de la boîte de dialogue **Options** de Microsoft Word). Pour en savoir plus, consultez l'article de documentation [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class CompatibilityOptions : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_AdjustLineHeightInTable](./get_adjustlineheightintable/)() | Ajouter le pas de ligne de la grille du [Document](../../aspose.words/document/) aux lignes dans les cellules de tableau. |
| [get_AlignTablesRowByRow](./get_aligntablesrowbyrow/)() | Aligner les lignes du tableau indépendamment. |
| [get_AllowSpaceOfSameStyleInTable](./get_allowspaceofsamestyleintable/)() | Autoriser l’espacement contextuel des paragraphes dans les [Tables](../../aspose.words.tables/). |
| [get_ApplyBreakingRules](./get_applybreakingrules/)() | Utiliser les règles de césure héritées pour l’éthiopien et l’amharique. |
| [get_AutofitToFirstFixedWidthCell](./get_autofittofirstfixedwidthcell/)() | Autoriser les colonnes du tableau à dépasser les largeurs préférées des cellules constituantes. |
| [get_AutoSpaceLikeWord95](./get_autospacelikeword95/)() | Émuler l’espacement plein‑largeur des caractères de Word 95. |
| [get_BalanceSingleByteDoubleByteWidth](./get_balancesinglebytedoublebytewidth/)() | Équilibrer les caractères à octet simple et à double octet. |
| [get_CachedColBalance](./get_cachedcolbalance/)() | Utiliser les informations [Paragraph](../../aspose.words/paragraph/) en cache pour l’équilibrage des colonnes. |
| [get_ConvMailMergeEsc](./get_convmailmergeesc/)() | Traiter le délimiteur de citation antislash comme deux guillemets. |
| [get_DisableOpenTypeFontFormattingFeatures](./get_disableopentypefontformattingfeatures/)() | Spécifie la désactivation des fonctionnalités de mise en forme OpenType. |
| [get_DisplayHangulFixedWidth](./get_displayhangulfixedwidth/)() | Utiliser toujours une largeur fixe pour les caractères Hangul. |
| [get_DoNotAutofitConstrainedTables](./get_donotautofitconstrainedtables/)() | Ne pas ajuster automatiquement les [Tables](../../aspose.words.tables/) pour les faire tenir à côté des objets enveloppés. |
| [get_DoNotBreakConstrainedForcedTable](./get_donotbreakconstrainedforcedtable/)() | Ne pas couper les lignes du tableau autour des [Tables](../../aspose.words.tables/) flottantes. |
| [get_DoNotBreakWrappedTables](./get_donotbreakwrappedtables/)() | Ne pas autoriser les [Tables](../../aspose.words.tables/) flottantes à se couper entre les pages. |
| [get_DoNotExpandShiftReturn](./get_donotexpandshiftreturn/)() | Ne pas justifier les lignes se terminant par un saut de ligne souple. |
| [get_DoNotLeaveBackslashAlone](./get_donotleavebackslashalone/)() | Convertir le antislash en signe Yen lorsqu’il est saisi. |
| [get_DoNotSnapToGridInCell](./get_donotsnaptogridincell/)() | Ne pas aligner sur la grille du [Document](../../aspose.words/document/) dans les cellules de tableau contenant des objets. |
| [get_DoNotSuppressIndentation](./get_donotsuppressindentation/)() | Ne pas ignorer les objets flottants lors du calcul de l’indentation du [Paragraph](../../aspose.words/paragraph/). |
| [get_DoNotSuppressParagraphBorders](./get_donotsuppressparagraphborders/)() | Ne supprimez pas les bordures du [Paragraph](../../aspose.words/paragraph/) à côté des cadres. |
| [get_DoNotUseEastAsianBreakRules](./get_donotuseeastasianbreakrules/)() | Ne compressez pas les caractères compressibles lors de l'utilisation de la grille du [Document](../../aspose.words/document/). |
| [get_DoNotUseHTMLParagraphAutoSpacing](./get_donotusehtmlparagraphautospacing/)() | Utilisez un espacement fixe du [Paragraph](../../aspose.words/paragraph/) pour le réglage automatique HTML. |
| [get_DoNotUseIndentAsNumberingTabStop](./get_donotuseindentasnumberingtabstop/)() | Ignorez le retrait suspendu lors de la création d'un arrêt de tabulation après la numérotation. |
| [get_DoNotVertAlignCellWithSp](./get_donotvertaligncellwithsp/)() | Ne pas aligner verticalement les cellules contenant des objets flottants. |
| [get_DoNotVertAlignInTxbx](./get_donotvertalignintxbx/)() | Ignorez l'alignement vertical dans les zones de texte. |
| [get_DoNotWrapTextWithPunct](./get_donotwraptextwithpunct/)() | Ne pas autoriser la ponctuation suspendue avec la grille de caractères. |
| [get_FootnoteLayoutLikeWW8](./get_footnotelayoutlikeww8/)() | Émuler le placement des notes de bas de page de Word 6.x/95/97. |
| [get_ForgetLastTabAlignment](./get_forgetlasttabalignment/)() | Ignorez la largeur du dernier arrêt de tabulation lors de l'alignement du [Paragraph](../../aspose.words/paragraph/) s'il n'est pas aligné à gauche. |
| [get_GrowAutofit](./get_growautofit/)() | Autorisez les [Tables](../../aspose.words.tables/) à s'ajuster automatiquement aux marges de la page. |
| [get_LayoutRawTableWidth](./get_layoutrawtablewidth/)() | Ignorez l'espace avant le tableau lors de la décision si le tableau doit envelopper l'objet flottant. |
| [get_LayoutTableRowsApart](./get_layouttablerowsapart/)() | Autorisez les lignes du tableau à envelopper les objets [Inline](../../aspose.words/inline/) de manière indépendante. |
| [get_LineWrapLikeWord6](./get_linewraplikeword6/)() | Émuler le retour à la ligne de Word 6.0 pour le texte est-asiatique. |
| [get_MWSmallCaps](./get_mwsmallcaps/)() | Émuler Word 5.x pour le formatage des petites majuscules sur Macintosh. |
| [get_NoColumnBalance](./get_nocolumnbalance/)() | Ne pas équilibrer les colonnes de texte à l'intérieur d'une [Section](../../aspose.words/section/). |
| [get_NoExtraLineSpacing](./get_noextralinespacing/)() | Ne pas centrer le contenu sur les lignes avec une hauteur de ligne exacte. |
| [get_NoLeading](./get_noleading/)() | Ne pas ajouter d'interligne entre les lignes de texte. |
| [get_NoSpaceRaiseLower](./get_nospaceraiselower/)() | Ne pas augmenter la hauteur de ligne pour le texte en exposant ou en indice. |
| [get_NoTabHangInd](./get_notabhangind/)() | Ne pas créer d'arrêt de tabulation personnalisé pour le retrait suspendu. |
| [get_OverrideTableStyleFontSizeAndJustification](./get_overridetablestylefontsizeandjustification/)() | Spécifie comment la hiérarchie des styles du document est évaluée. |
| [get_PrintBodyTextBeforeHeader](./get_printbodytextbeforeheader/)() | Imprimez le texte du [Body](../../aspose.words/body/) avant le contenu de l'en-tête/pied de page. |
| [get_PrintColBlack](./get_printcolblack/)() | Imprimez les couleurs en noir et blanc sans tramage. |
| [get_SelectFldWithFirstOrLastChar](./get_selectfldwithfirstorlastchar/)() | Sélectionnez le champ lorsque le premier ou le dernier caractère est sélectionné. |
| [get_ShapeLayoutLikeWW8](./get_shapelayoutlikeww8/)() | Émuler le retour à la ligne du texte de Word 97 autour des objets flottants. |
| [get_ShowBreaksInFrames](./get_showbreaksinframes/)() | Affichez les sauts de page/colonne présents dans les cadres. |
| [get_SpaceForUL](./get_spaceforul/)() | Ajouter un espace supplémentaire sous la ligne de base pour le texte asiatique souligné. |
| [get_SpacingInWholePoints](./get_spacinginwholepoints/)() | N'étendre/condensez le texte que par des points entiers. |
| [get_SplitPgBreakAndParaMark](./get_splitpgbreakandparamark/)() | Toujours déplacer la marque de [Paragraph](../../aspose.words/paragraph/) vers la page après un saut de page. |
| [get_SubFontBySize](./get_subfontbysize/)() | Augmenter la priorité de la taille de [Font](../../aspose.words/font/) lors de la substitution de [Font](../../aspose.words/font/). |
| [get_SuppressBottomSpacing](./get_suppressbottomspacing/)() | Ignorer la hauteur de ligne exacte pour la dernière ligne de la page. |
| [get_SuppressSpacingAtTopOfPage](./get_suppressspacingattopofpage/)() | Ignorer la hauteur de ligne minimale pour la première ligne de la page. |
| [get_SuppressSpBfAfterPgBrk](./get_suppressspbfafterpgbrk/)() | Ne pas utiliser d'espace avant sur la première ligne après un saut de page. |
| [get_SuppressTopSpacing](./get_suppresstopspacing/)() | Ignorer la hauteur de ligne minimale et exacte pour la première ligne de la page. |
| [get_SuppressTopSpacingWP](./get_suppresstopspacingwp/)() | Émuler l'espacement des lignes de WordPerfect 5.x. |
| [get_SwapBordersFacingPgs](./get_swapbordersfacingpgs/)() | Échanger les bordures de [Paragraph](../../aspose.words/paragraph/) sur les pages impaires. |
| [get_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./get_swapinsideandoutsideformirrorindentsandrelativepositioning/)() | Spécifie d'échanger l'intérieur et l'extérieur pour les retraits en miroir et le positionnement relatif. |
| [get_TransparentMetafiles](./get_transparentmetafiles/)() | Spécifie de ne pas blanchir la zone derrière les images de métafichier. |
| [get_TruncateFontHeightsLikeWP6](./get_truncatefontheightslikewp6/)() | Émuler le calcul de la hauteur de [Font](../../aspose.words/font/) de WordPerfect 6.x. |
| [get_UICompat97To2003](./get_uicompat97to2003/)() | Vrai pour désactiver les fonctionnalités UI qui ne sont pas compatibles avec Word97-2003. La valeur par défaut est **false**. |
| [get_UlTrailSpace](./get_ultrailspace/)() | Souligner tous les espaces de fin. |
| [get_UnderlineTabInNumList](./get_underlinetabinnumlist/)() | Souligner le caractère suivant après la numérotation. |
| [get_UseAltKinsokuLineBreakRules](./get_usealtkinsokulinebreakrules/)() | Utiliser un jeu alternatif de règles de césure de lignes asiatiques. |
| [get_UseAnsiKerningPairs](./get_useansikerningpairs/)() | Utiliser les paires de crénage ANSI provenant de [Fonts](../../aspose.words.fonts/). |
| [get_UseFELayout](./get_usefelayout/)() | Ne pas contourner le code de [Layout](../../aspose.words.layout/) des scripts asiatiques/complexes. |
| [get_UseNormalStyleForList](./get_usenormalstyleforlist/)() | Ne pas appliquer automatiquement la liste [Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) au texte à puces/numéroté. |
| [get_UsePrinterMetrics](./get_useprintermetrics/)() | Utiliser les métriques de l'imprimante pour afficher les documents. |
| [get_UseSingleBorderforContiguousCells](./get_usesingleborderforcontiguouscells/)() | Utiliser des règles simplifiées pour les conflits de [Border](../../aspose.words/border/) de tableau. |
| [get_UseWord2002TableStyleRules](./get_useword2002tablestylerules/)() | Émuler les règles de [Style](../../aspose.words/style/) de tableau de Word 2002. |
| [get_UseWord2010TableStyleRules](./get_useword2010tablestylerules/)() | Spécifie d'utiliser les règles de style de tableau Word2010. |
| [get_UseWord97LineBreakRules](./get_useword97linebreakrules/)() | Émuler la césure de lignes asiatiques de Word 97. |
| [get_WPJustification](./get_wpjustification/)() | Émuler WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) Justification. |
| [get_WPSpaceWidth](./get_wpspacewidth/)() | Spécifie s'il faut définir la largeur d'un espace comme c'est le cas dans WordPerfect 5.x. |
| [get_WrapTrailSpaces](./get_wraptrailspaces/)() | Enroulement de ligne des espaces de fin. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OptimizeFor](./optimizefor/)(Aspose::Words::Settings::MsWordVersion) | Permet d'optimiser le contenu du document ainsi que le comportement par défaut d'Aspose.Words pour des versions particulières de MS Word. Utilisez cette méthode pour empêcher MS Word d'afficher le ruban « Compatibility mode » lors du chargement du document. (Notez que vous devrez peut-être également définir la propriété [Compliance](../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) sur [Iso2950_2008_Transitional](../../aspose.words.saving/ooxmlcompliance/) ou une version supérieure.) |
| [set_AdjustLineHeightInTable](./set_adjustlineheightintable/)(bool) | Ajouter le pas de ligne de la grille du [Document](../../aspose.words/document/) aux lignes dans les cellules de tableau. |
| [set_AlignTablesRowByRow](./set_aligntablesrowbyrow/)(bool) | Aligner les lignes du tableau indépendamment. |
| [set_AllowSpaceOfSameStyleInTable](./set_allowspaceofsamestyleintable/)(bool) | Autoriser l’espacement contextuel des paragraphes dans les [Tables](../../aspose.words.tables/). |
| [set_ApplyBreakingRules](./set_applybreakingrules/)(bool) | Utiliser les règles de césure héritées pour l’éthiopien et l’amharique. |
| [set_AutofitToFirstFixedWidthCell](./set_autofittofirstfixedwidthcell/)(bool) | Autoriser les colonnes du tableau à dépasser les largeurs préférées des cellules constituantes. |
| [set_AutoSpaceLikeWord95](./set_autospacelikeword95/)(bool) | Émuler l’espacement plein‑largeur des caractères de Word 95. |
| [set_BalanceSingleByteDoubleByteWidth](./set_balancesinglebytedoublebytewidth/)(bool) | Équilibrer les caractères à octet simple et à double octet. |
| [set_CachedColBalance](./set_cachedcolbalance/)(bool) | Utiliser les informations [Paragraph](../../aspose.words/paragraph/) en cache pour l’équilibrage des colonnes. |
| [set_ConvMailMergeEsc](./set_convmailmergeesc/)(bool) | Traiter le délimiteur de citation antislash comme deux guillemets. |
| [set_DisableOpenTypeFontFormattingFeatures](./set_disableopentypefontformattingfeatures/)(bool) | Spécifie la désactivation des fonctionnalités de mise en forme OpenType. |
| [set_DisplayHangulFixedWidth](./set_displayhangulfixedwidth/)(bool) | Utiliser toujours une largeur fixe pour les caractères Hangul. |
| [set_DoNotAutofitConstrainedTables](./set_donotautofitconstrainedtables/)(bool) | Ne pas ajuster automatiquement les [Tables](../../aspose.words.tables/) pour les faire tenir à côté des objets enveloppés. |
| [set_DoNotBreakConstrainedForcedTable](./set_donotbreakconstrainedforcedtable/)(bool) | Ne pas couper les lignes du tableau autour des [Tables](../../aspose.words.tables/) flottantes. |
| [set_DoNotBreakWrappedTables](./set_donotbreakwrappedtables/)(bool) | Ne pas autoriser les [Tables](../../aspose.words.tables/) flottantes à se couper entre les pages. |
| [set_DoNotExpandShiftReturn](./set_donotexpandshiftreturn/)(bool) | Ne pas justifier les lignes se terminant par un saut de ligne souple. |
| [set_DoNotLeaveBackslashAlone](./set_donotleavebackslashalone/)(bool) | Convertir le antislash en signe Yen lorsqu’il est saisi. |
| [set_DoNotSnapToGridInCell](./set_donotsnaptogridincell/)(bool) | Ne pas aligner sur la grille du [Document](../../aspose.words/document/) dans les cellules de tableau contenant des objets. |
| [set_DoNotSuppressIndentation](./set_donotsuppressindentation/)(bool) | Ne pas ignorer les objets flottants lors du calcul de l’indentation du [Paragraph](../../aspose.words/paragraph/). |
| [set_DoNotSuppressParagraphBorders](./set_donotsuppressparagraphborders/)(bool) | Ne supprimez pas les bordures du [Paragraph](../../aspose.words/paragraph/) à côté des cadres. |
| [set_DoNotUseEastAsianBreakRules](./set_donotuseeastasianbreakrules/)(bool) | Ne compressez pas les caractères compressibles lors de l'utilisation de la grille du [Document](../../aspose.words/document/). |
| [set_DoNotUseHTMLParagraphAutoSpacing](./set_donotusehtmlparagraphautospacing/)(bool) | Utilisez un espacement fixe du [Paragraph](../../aspose.words/paragraph/) pour le réglage automatique HTML. |
| [set_DoNotUseIndentAsNumberingTabStop](./set_donotuseindentasnumberingtabstop/)(bool) | Ignorez le retrait suspendu lors de la création d'un arrêt de tabulation après la numérotation. |
| [set_DoNotVertAlignCellWithSp](./set_donotvertaligncellwithsp/)(bool) | Ne pas aligner verticalement les cellules contenant des objets flottants. |
| [set_DoNotVertAlignInTxbx](./set_donotvertalignintxbx/)(bool) | Ignorez l'alignement vertical dans les zones de texte. |
| [set_DoNotWrapTextWithPunct](./set_donotwraptextwithpunct/)(bool) | Ne pas autoriser la ponctuation suspendue avec la grille de caractères. |
| [set_FootnoteLayoutLikeWW8](./set_footnotelayoutlikeww8/)(bool) | Émuler le placement des notes de bas de page de Word 6.x/95/97. |
| [set_ForgetLastTabAlignment](./set_forgetlasttabalignment/)(bool) | Ignorez la largeur du dernier arrêt de tabulation lors de l'alignement du [Paragraph](../../aspose.words/paragraph/) s'il n'est pas aligné à gauche. |
| [set_GrowAutofit](./set_growautofit/)(bool) | Autorisez les [Tables](../../aspose.words.tables/) à s'ajuster automatiquement aux marges de la page. |
| [set_LayoutRawTableWidth](./set_layoutrawtablewidth/)(bool) | Ignorez l'espace avant le tableau lors de la décision si le tableau doit envelopper l'objet flottant. |
| [set_LayoutTableRowsApart](./set_layouttablerowsapart/)(bool) | Autorisez les lignes du tableau à envelopper les objets [Inline](../../aspose.words/inline/) de manière indépendante. |
| [set_LineWrapLikeWord6](./set_linewraplikeword6/)(bool) | Émuler le retour à la ligne de Word 6.0 pour le texte est-asiatique. |
| [set_MWSmallCaps](./set_mwsmallcaps/)(bool) | Émuler Word 5.x pour le formatage des petites majuscules sur Macintosh. |
| [set_NoColumnBalance](./set_nocolumnbalance/)(bool) | Ne pas équilibrer les colonnes de texte à l'intérieur d'une [Section](../../aspose.words/section/). |
| [set_NoExtraLineSpacing](./set_noextralinespacing/)(bool) | Ne pas centrer le contenu sur les lignes avec une hauteur de ligne exacte. |
| [set_NoLeading](./set_noleading/)(bool) | Ne pas ajouter d'interligne entre les lignes de texte. |
| [set_NoSpaceRaiseLower](./set_nospaceraiselower/)(bool) | Ne pas augmenter la hauteur de ligne pour le texte en exposant ou en indice. |
| [set_NoTabHangInd](./set_notabhangind/)(bool) | Ne pas créer d'arrêt de tabulation personnalisé pour le retrait suspendu. |
| [set_OverrideTableStyleFontSizeAndJustification](./set_overridetablestylefontsizeandjustification/)(bool) | Spécifie comment la hiérarchie des styles du document est évaluée. |
| [set_PrintBodyTextBeforeHeader](./set_printbodytextbeforeheader/)(bool) | Imprimez le texte du [Body](../../aspose.words/body/) avant le contenu de l'en-tête/pied de page. |
| [set_PrintColBlack](./set_printcolblack/)(bool) | Imprimez les couleurs en noir et blanc sans tramage. |
| [set_SelectFldWithFirstOrLastChar](./set_selectfldwithfirstorlastchar/)(bool) | Sélectionnez le champ lorsque le premier ou le dernier caractère est sélectionné. |
| [set_ShapeLayoutLikeWW8](./set_shapelayoutlikeww8/)(bool) | Émuler le retour à la ligne du texte de Word 97 autour des objets flottants. |
| [set_ShowBreaksInFrames](./set_showbreaksinframes/)(bool) | Affichez les sauts de page/colonne présents dans les cadres. |
| [set_SpaceForUL](./set_spaceforul/)(bool) | Ajouter un espace supplémentaire sous la ligne de base pour le texte asiatique souligné. |
| [set_SpacingInWholePoints](./set_spacinginwholepoints/)(bool) | N'étendre/condensez le texte que par des points entiers. |
| [set_SplitPgBreakAndParaMark](./set_splitpgbreakandparamark/)(bool) | Toujours déplacer la marque de [Paragraph](../../aspose.words/paragraph/) vers la page après un saut de page. |
| [set_SubFontBySize](./set_subfontbysize/)(bool) | Augmenter la priorité de la taille de [Font](../../aspose.words/font/) lors de la substitution de [Font](../../aspose.words/font/). |
| [set_SuppressBottomSpacing](./set_suppressbottomspacing/)(bool) | Ignorer la hauteur de ligne exacte pour la dernière ligne de la page. |
| [set_SuppressSpacingAtTopOfPage](./set_suppressspacingattopofpage/)(bool) | Ignorer la hauteur de ligne minimale pour la première ligne de la page. |
| [set_SuppressSpBfAfterPgBrk](./set_suppressspbfafterpgbrk/)(bool) | Ne pas utiliser d'espace avant sur la première ligne après un saut de page. |
| [set_SuppressTopSpacing](./set_suppresstopspacing/)(bool) | Ignorer la hauteur de ligne minimale et exacte pour la première ligne de la page. |
| [set_SuppressTopSpacingWP](./set_suppresstopspacingwp/)(bool) | Émuler l'espacement des lignes de WordPerfect 5.x. |
| [set_SwapBordersFacingPgs](./set_swapbordersfacingpgs/)(bool) | Échanger les bordures de [Paragraph](../../aspose.words/paragraph/) sur les pages impaires. |
| [set_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./set_swapinsideandoutsideformirrorindentsandrelativepositioning/)(bool) | Spécifie d'échanger l'intérieur et l'extérieur pour les retraits en miroir et le positionnement relatif. |
| [set_TransparentMetafiles](./set_transparentmetafiles/)(bool) | Spécifie de ne pas blanchir la zone derrière les images de métafichier. |
| [set_TruncateFontHeightsLikeWP6](./set_truncatefontheightslikewp6/)(bool) | Émuler le calcul de la hauteur de [Font](../../aspose.words/font/) de WordPerfect 6.x. |
| [set_UICompat97To2003](./set_uicompat97to2003/)(bool) | Vrai pour désactiver les fonctionnalités UI qui ne sont pas compatibles avec Word97-2003. La valeur par défaut est **false**. |
| [set_UlTrailSpace](./set_ultrailspace/)(bool) | Souligner tous les espaces de fin. |
| [set_UnderlineTabInNumList](./set_underlinetabinnumlist/)(bool) | Souligner le caractère suivant après la numérotation. |
| [set_UseAltKinsokuLineBreakRules](./set_usealtkinsokulinebreakrules/)(bool) | Utiliser un jeu alternatif de règles de césure de lignes asiatiques. |
| [set_UseAnsiKerningPairs](./set_useansikerningpairs/)(bool) | Utiliser les paires de crénage ANSI provenant de [Fonts](../../aspose.words.fonts/). |
| [set_UseFELayout](./set_usefelayout/)(bool) | Ne pas contourner le code de [Layout](../../aspose.words.layout/) des scripts asiatiques/complexes. |
| [set_UseNormalStyleForList](./set_usenormalstyleforlist/)(bool) | Ne pas appliquer automatiquement la liste [Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) au texte à puces/numéroté. |
| [set_UsePrinterMetrics](./set_useprintermetrics/)(bool) | Utiliser les métriques de l'imprimante pour afficher les documents. |
| [set_UseSingleBorderforContiguousCells](./set_usesingleborderforcontiguouscells/)(bool) | Utiliser des règles simplifiées pour les conflits de [Border](../../aspose.words/border/) de tableau. |
| [set_UseWord2002TableStyleRules](./set_useword2002tablestylerules/)(bool) | Émuler les règles de [Style](../../aspose.words/style/) de tableau de Word 2002. |
| [set_UseWord2010TableStyleRules](./set_useword2010tablestylerules/)(bool) | Spécifie d'utiliser les règles de style de tableau Word2010. |
| [set_UseWord97LineBreakRules](./set_useword97linebreakrules/)(bool) | Émuler la césure de lignes asiatiques de Word 97. |
| [set_WPJustification](./set_wpjustification/)(bool) | Émuler WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) Justification. |
| [set_WPSpaceWidth](./set_wpspacewidth/)(bool) | Spécifie s'il faut définir la largeur d'un espace comme c'est le cas dans WordPerfect 5.x. |
| [set_WrapTrailSpaces](./set_wraptrailspaces/)(bool) | Enroulement de ligne des espaces de fin. |
| static [Type](./type/)() |  |

## Exemples



Montre comment définir une spécification de conformité OOXML pour un document enregistré afin de s'y conformer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Si nous configurons les options de compatibilité pour être conformes à Microsoft Word 2003,
// l'insertion d'une image définira sa forme en utilisant VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// La norme OOXML "ISO/IEC 29500:2008" ne prend pas en charge les formes VML.
// Si nous définissons la propriété "Compliance" de l'objet SaveOptions sur "OoxmlCompliance.Iso29500_2008_Strict",
// tout document que nous enregistrons en passant cet objet devra suivre cette norme.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme en utilisant DML pour se conformer à la norme OOXML "ISO/IEC 29500:2008".
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


Montre comment aligner verticalement le contenu texte d'une zone de texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Top" pour
// aligner le texte de cette zone de texte avec le côté supérieur de la forme.
// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Middle" pour
// aligner le texte de cette zone de texte au centre de la forme.
// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Bottom" pour
// aligner le texte de cette zone de texte au bas de la forme.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// L'alignement vertical du texte à l'intérieur des zones de texte est disponible à partir de Microsoft Word 2007.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Voir aussi

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
