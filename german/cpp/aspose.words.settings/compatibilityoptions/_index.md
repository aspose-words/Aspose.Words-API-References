---
title: "Aspose::Words::Settings::CompatibilityOptions Klasse"
linktitle: "CompatibilityOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::CompatibilityOptions Klasse. Enthält Kompatibilitätsoptionen (das heißt, die vom Benutzer im Reiter Kompatibilität des Optionsdialogs in Microsoft Word eingegebenen Einstellungen). Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.settings/compatibilityoptions/
---
## CompatibilityOptions class


Enthält Kompatibilitätsoptionen (das heißt, die vom Benutzer eingegebenen Einstellungen auf der Registerkarte **Compatibility** im Dialogfeld **Options** in Microsoft Word). Weitere Informationen finden Sie im Dokumentationsartikel [Dateiformat erkennen und Formatkompatibilität prüfen](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class CompatibilityOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_AdjustLineHeightInTable](./get_adjustlineheightintable/)() | Fügen Sie dem [Document](../../aspose.words/document/) Rasterlinienabstand zu Zeilen in Tabellenzellen hinzu. |
| [get_AlignTablesRowByRow](./get_aligntablesrowbyrow/)() | Tabellenzeilen unabhängig ausrichten. |
| [get_AllowSpaceOfSameStyleInTable](./get_allowspaceofsamestyleintable/)() | Erlauben Sie kontextabhängige Abstände von Absätzen in [Tables](../../aspose.words.tables/). |
| [get_ApplyBreakingRules](./get_applybreakingrules/)() | Verwenden Sie die alten Zeilenumbruchregeln für Äthiopisch und Amharisch. |
| [get_AutofitToFirstFixedWidthCell](./get_autofittofirstfixedwidthcell/)() | Erlauben Sie Tabellen­spalten, die bevorzugten Breiten der enthaltenen Zellen zu überschreiten. |
| [get_AutoSpaceLikeWord95](./get_autospacelikeword95/)() | Emulieren Sie die Vollbreiten‑Zeichenabstände von Word 95. |
| [get_BalanceSingleByteDoubleByteWidth](./get_balancesinglebytedoublebytewidth/)() | Balancieren Sie ein‑Byte‑ und zwei‑Byte‑Zeichen aus. |
| [get_CachedColBalance](./get_cachedcolbalance/)() | Verwenden Sie zwischengespeicherte [Paragraph](../../aspose.words/paragraph/) Informationen zum Spaltenausgleich. |
| [get_ConvMailMergeEsc](./get_convmailmergeesc/)() | Behandeln Sie das Backslash‑Zitat‑Trennzeichen als zwei Anführungszeichen. |
| [get_DisableOpenTypeFontFormattingFeatures](./get_disableopentypefontformattingfeatures/)() | Gibt an, OpenType‑Schriftformatierungsfunktionen zu deaktivieren. |
| [get_DisplayHangulFixedWidth](./get_displayhangulfixedwidth/)() | Verwenden Sie immer feste Breite für Hangul‑Zeichen. |
| [get_DoNotAutofitConstrainedTables](./get_donotautofitconstrainedtables/)() | AutoFit von [Tables](../../aspose.words.tables/) nicht durchführen, damit sie neben umflossenen Objekten passen. |
| [get_DoNotBreakConstrainedForcedTable](./get_donotbreakconstrainedforcedtable/)() | Tabellenzeilen nicht um schwebende [Tables](../../aspose.words.tables/) herum brechen. |
| [get_DoNotBreakWrappedTables](./get_donotbreakwrappedtables/)() | Schwebenden [Tables](../../aspose.words.tables/) nicht erlauben, über Seiten hinweg zu brechen. |
| [get_DoNotExpandShiftReturn](./get_donotexpandshiftreturn/)() | Zeilen, die mit einem weichen Zeilenumbruch enden, nicht ausrichten. |
| [get_DoNotLeaveBackslashAlone](./get_donotleavebackslashalone/)() | Backslash bei Eingabe in das Yen‑Zeichen umwandeln. |
| [get_DoNotSnapToGridInCell](./get_donotsnaptogridincell/)() | In Tabellenzellen mit Objekten nicht am [Document](../../aspose.words/document/) Raster einrasten. |
| [get_DoNotSuppressIndentation](./get_donotsuppressindentation/)() | Schwebende Objekte beim Berechnen der Einrückung von [Paragraph](../../aspose.words/paragraph/) nicht ignorieren. |
| [get_DoNotSuppressParagraphBorders](./get_donotsuppressparagraphborders/)() | Grenzen von [Paragraph](../../aspose.words/paragraph/) neben Rahmen nicht unterdrücken. |
| [get_DoNotUseEastAsianBreakRules](./get_donotuseeastasianbreakrules/)() | Komprimierbare Zeichen beim Verwenden des [Document](../../aspose.words/document/) Rasters nicht komprimieren. |
| [get_DoNotUseHTMLParagraphAutoSpacing](./get_donotusehtmlparagraphautospacing/)() | Verwenden Sie festen [Paragraph](../../aspose.words/paragraph/) Abstand für die HTML-Autoeinstellung. |
| [get_DoNotUseIndentAsNumberingTabStop](./get_donotuseindentasnumberingtabstop/)() | Ignorieren Sie hängenden Einzug beim Erstellen eines Tabstopps nach der Nummerierung. |
| [get_DoNotVertAlignCellWithSp](./get_donotvertaligncellwithsp/)() | Richten Sie Zellen, die schwebende Objekte enthalten, nicht vertikal aus. |
| [get_DoNotVertAlignInTxbx](./get_donotvertalignintxbx/)() | Ignorieren Sie die vertikale Ausrichtung in Textfeldern. |
| [get_DoNotWrapTextWithPunct](./get_donotwraptextwithpunct/)() | Erlauben Sie hängende Interpunktion nicht mit dem Zeichenraster. |
| [get_FootnoteLayoutLikeWW8](./get_footnotelayoutlikeww8/)() | Emulieren Sie die Fußnotenanordnung von Word 6.x/95/97. |
| [get_ForgetLastTabAlignment](./get_forgetlasttabalignment/)() | Ignorieren Sie die Breite des letzten Tabstopps beim Ausrichten des [Paragraph](../../aspose.words/paragraph/), wenn er nicht linksbündig ist. |
| [get_GrowAutofit](./get_growautofit/)() | Erlauben Sie, dass [Tables](../../aspose.words.tables/) automatisch in die Seitenränder passen. |
| [get_LayoutRawTableWidth](./get_layoutrawtablewidth/)() | Ignorieren Sie den Abstand vor der Tabelle, wenn entschieden wird, ob die Tabelle ein schwebendes Objekt umbrechen soll. |
| [get_LayoutTableRowsApart](./get_layouttablerowsapart/)() | Erlauben Sie, dass Tabellenzeilen [Inline](../../aspose.words/inline/) Objekte unabhängig umbrechen. |
| [get_LineWrapLikeWord6](./get_linewraplikeword6/)() | Emulieren Sie den Zeilenumbruch von Word 6.0 für ostasiatischen Text. |
| [get_MWSmallCaps](./get_mwsmallcaps/)() | Emulieren Sie Word 5.x für die Small-Caps-Formatierung auf dem Macintosh. |
| [get_NoColumnBalance](./get_nocolumnbalance/)() | Balancieren Sie Textspalten innerhalb einer [Section](../../aspose.words/section/) nicht. |
| [get_NoExtraLineSpacing](./get_noextralinespacing/)() | Zentrieren Sie Inhalte nicht auf Zeilen mit exakter Zeilenhöhe. |
| [get_NoLeading](./get_noleading/)() | Fügen Sie keinen Zeilenabstand zwischen Textzeilen hinzu. |
| [get_NoSpaceRaiseLower](./get_nospaceraiselower/)() | Vergrößern Sie die Zeilenhöhe nicht für hoch- oder tiefgestellten Text. |
| [get_NoTabHangInd](./get_notabhangind/)() | Erstellen Sie keinen benutzerdefinierten Tabstopp für hängenden Einzug. |
| [get_OverrideTableStyleFontSizeAndJustification](./get_overridetablestylefontsizeandjustification/)() | Gibt an, wie die Stilhierarchie des Dokuments ausgewertet wird. |
| [get_PrintBodyTextBeforeHeader](./get_printbodytextbeforeheader/)() | Drucken Sie den [Body](../../aspose.words/body/) Text vor den Kopf-/Fußzeileninhalten. |
| [get_PrintColBlack](./get_printcolblack/)() | Drucken Sie Farben als Schwarz‑Weiß ohne Dithering. |
| [get_SelectFldWithFirstOrLastChar](./get_selectfldwithfirstorlastchar/)() | Wählen Sie das Feld aus, wenn das erste oder letzte Zeichen ausgewählt ist. |
| [get_ShapeLayoutLikeWW8](./get_shapelayoutlikeww8/)() | Emulieren Sie den Textumbruch von Word 97 um schwebende Objekte. |
| [get_ShowBreaksInFrames](./get_showbreaksinframes/)() | Zeigen Sie Seiten‑/Spaltenumbrüche an, die in Rahmen vorhanden sind. |
| [get_SpaceForUL](./get_spaceforul/)() | Fügen Sie zusätzlichen Abstand unter der Grundlinie für unterstrichenen ostasiatischen Text hinzu. |
| [get_SpacingInWholePoints](./get_spacinginwholepoints/)() | Erweitern/Kontrahieren Sie Text nur um ganze Punkte. |
| [get_SplitPgBreakAndParaMark](./get_splitpgbreakandparamark/)() | Immer das [Paragraph](../../aspose.words/paragraph/) Mark auf die Seite nach einem Seitenumbruch verschieben. |
| [get_SubFontBySize](./get_subfontbysize/)() | Priorität der [Font](../../aspose.words/font/) Größe während der [Font](../../aspose.words/font/) Substitution erhöhen. |
| [get_SuppressBottomSpacing](./get_suppressbottomspacing/)() | Exakte Zeilenhöhe für die letzte Zeile auf der Seite ignorieren. |
| [get_SuppressSpacingAtTopOfPage](./get_suppressspacingattopofpage/)() | Minimale Zeilenhöhe für die erste Zeile auf der Seite ignorieren. |
| [get_SuppressSpBfAfterPgBrk](./get_suppressspbfafterpgbrk/)() | Kein Leerzeichen vor der ersten Zeile nach einem Seitenumbruch verwenden. |
| [get_SuppressTopSpacing](./get_suppresstopspacing/)() | Minimale und exakte Zeilenhöhe für die erste Zeile auf der Seite ignorieren. |
| [get_SuppressTopSpacingWP](./get_suppresstopspacingwp/)() | WordPerfect 5.x Zeilenabstand emulieren. |
| [get_SwapBordersFacingPgs](./get_swapbordersfacingpgs/)() | [Paragraph](../../aspose.words/paragraph/) Rahmen auf ungeraden Seiten vertauschen. |
| [get_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./get_swapinsideandoutsideformirrorindentsandrelativepositioning/)() | Gibt an, innen und außen für Spiegel‑Einzüge und relative Positionierung zu vertauschen. |
| [get_TransparentMetafiles](./get_transparentmetafiles/)() | Gibt an, den Bereich hinter Metadatei‑Bildern nicht zu leeren. |
| [get_TruncateFontHeightsLikeWP6](./get_truncatefontheightslikewp6/)() | WordPerfect 6.x [Font](../../aspose.words/font/) Höhenberechnung emulieren. |
| [get_UICompat97To2003](./get_uicompat97to2003/)() | Wahr, um UI‑Funktionalität zu deaktivieren, die nicht mit Word97-2003 kompatibel ist. Standardwert ist **false**. |
| [get_UlTrailSpace](./get_ultrailspace/)() | Alle nachfolgenden Leerzeichen unterstreichen. |
| [get_UnderlineTabInNumList](./get_underlinetabinnumlist/)() | Nachfolgendes Zeichen nach der Nummerierung unterstreichen. |
| [get_UseAltKinsokuLineBreakRules](./get_usealtkinsokulinebreakrules/)() | Alternatives Set von Ostasiatischen Zeilenumbruch‑Regeln verwenden. |
| [get_UseAnsiKerningPairs](./get_useansikerningpairs/)() | ANSI‑Kerning‑Paare aus [Fonts](../../aspose.words.fonts/) verwenden. |
| [get_UseFELayout](./get_usefelayout/)() | Den Ostasiatisch/Komplex‑Skript [Layout](../../aspose.words.layout/) Code nicht umgehen. |
| [get_UseNormalStyleForList](./get_usenormalstyleforlist/)() | Listen-[Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) nicht automatisch auf Aufzählungs‑/Nummerierungstext anwenden. |
| [get_UsePrinterMetrics](./get_useprintermetrics/)() | Drucker‑Metriken verwenden, um Dokumente anzuzeigen. |
| [get_UseSingleBorderforContiguousCells](./get_usesingleborderforcontiguouscells/)() | Vereinfachte Regeln für Tabellen-[Border](../../aspose.words/border/) Konflikte verwenden. |
| [get_UseWord2002TableStyleRules](./get_useword2002tablestylerules/)() | Word 2002 Tabellen-[Style](../../aspose.words/style/) Regeln emulieren. |
| [get_UseWord2010TableStyleRules](./get_useword2010tablestylerules/)() | Gibt an, Word2010 Tabellen‑Stilregeln zu verwenden. |
| [get_UseWord97LineBreakRules](./get_useword97linebreakrules/)() | Word 97 Ostasiatischen Zeilenumbruch emulieren. |
| [get_WPJustification](./get_wpjustification/)() | WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) Blocksatz emulieren. |
| [get_WPSpaceWidth](./get_wpspacewidth/)() | Gibt an, ob die Breite eines Leerzeichens wie in WordPerfect 5.x festgelegt werden soll. |
| [get_WrapTrailSpaces](./get_wraptrailspaces/)() | Zeilenumbruch nachfolgenden Leerzeichen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OptimizeFor](./optimizefor/)(Aspose::Words::Settings::MsWordVersion) | Ermöglicht die Optimierung des Dokumentinhalts sowie des Standardverhaltens von Aspose.Words für bestimmte Versionen von MS Word. Verwenden Sie diese Methode, um zu verhindern, dass MS Word beim Laden des Dokuments das "Compatibility mode"-Menüband anzeigt. (Hinweis, dass Sie möglicherweise auch die [Compliance](../../aspose.words.saving/ooxmlsaveoptions/get_compliance/) Eigenschaft auf [Iso29500_2008_Transitional](../../aspose.words.saving/ooxmlcompliance/) oder höher setzen müssen.) |
| [set_AdjustLineHeightInTable](./set_adjustlineheightintable/)(bool) | Fügen Sie dem [Document](../../aspose.words/document/) Rasterlinienabstand zu Zeilen in Tabellenzellen hinzu. |
| [set_AlignTablesRowByRow](./set_aligntablesrowbyrow/)(bool) | Tabellenzeilen unabhängig ausrichten. |
| [set_AllowSpaceOfSameStyleInTable](./set_allowspaceofsamestyleintable/)(bool) | Erlauben Sie kontextabhängige Abstände von Absätzen in [Tables](../../aspose.words.tables/). |
| [set_ApplyBreakingRules](./set_applybreakingrules/)(bool) | Verwenden Sie die alten Zeilenumbruchregeln für Äthiopisch und Amharisch. |
| [set_AutofitToFirstFixedWidthCell](./set_autofittofirstfixedwidthcell/)(bool) | Erlauben Sie Tabellen­spalten, die bevorzugten Breiten der enthaltenen Zellen zu überschreiten. |
| [set_AutoSpaceLikeWord95](./set_autospacelikeword95/)(bool) | Emulieren Sie die Vollbreiten‑Zeichenabstände von Word 95. |
| [set_BalanceSingleByteDoubleByteWidth](./set_balancesinglebytedoublebytewidth/)(bool) | Balancieren Sie ein‑Byte‑ und zwei‑Byte‑Zeichen aus. |
| [set_CachedColBalance](./set_cachedcolbalance/)(bool) | Verwenden Sie zwischengespeicherte [Paragraph](../../aspose.words/paragraph/) Informationen zum Spaltenausgleich. |
| [set_ConvMailMergeEsc](./set_convmailmergeesc/)(bool) | Behandeln Sie das Backslash‑Zitat‑Trennzeichen als zwei Anführungszeichen. |
| [set_DisableOpenTypeFontFormattingFeatures](./set_disableopentypefontformattingfeatures/)(bool) | Gibt an, OpenType‑Schriftformatierungsfunktionen zu deaktivieren. |
| [set_DisplayHangulFixedWidth](./set_displayhangulfixedwidth/)(bool) | Verwenden Sie immer feste Breite für Hangul‑Zeichen. |
| [set_DoNotAutofitConstrainedTables](./set_donotautofitconstrainedtables/)(bool) | AutoFit von [Tables](../../aspose.words.tables/) nicht durchführen, damit sie neben umflossenen Objekten passen. |
| [set_DoNotBreakConstrainedForcedTable](./set_donotbreakconstrainedforcedtable/)(bool) | Tabellenzeilen nicht um schwebende [Tables](../../aspose.words.tables/) herum brechen. |
| [set_DoNotBreakWrappedTables](./set_donotbreakwrappedtables/)(bool) | Schwebenden [Tables](../../aspose.words.tables/) nicht erlauben, über Seiten hinweg zu brechen. |
| [set_DoNotExpandShiftReturn](./set_donotexpandshiftreturn/)(bool) | Zeilen, die mit einem weichen Zeilenumbruch enden, nicht ausrichten. |
| [set_DoNotLeaveBackslashAlone](./set_donotleavebackslashalone/)(bool) | Backslash bei Eingabe in das Yen‑Zeichen umwandeln. |
| [set_DoNotSnapToGridInCell](./set_donotsnaptogridincell/)(bool) | In Tabellenzellen mit Objekten nicht am [Document](../../aspose.words/document/) Raster einrasten. |
| [set_DoNotSuppressIndentation](./set_donotsuppressindentation/)(bool) | Schwebende Objekte beim Berechnen der Einrückung von [Paragraph](../../aspose.words/paragraph/) nicht ignorieren. |
| [set_DoNotSuppressParagraphBorders](./set_donotsuppressparagraphborders/)(bool) | Grenzen von [Paragraph](../../aspose.words/paragraph/) neben Rahmen nicht unterdrücken. |
| [set_DoNotUseEastAsianBreakRules](./set_donotuseeastasianbreakrules/)(bool) | Komprimierbare Zeichen beim Verwenden des [Document](../../aspose.words/document/) Rasters nicht komprimieren. |
| [set_DoNotUseHTMLParagraphAutoSpacing](./set_donotusehtmlparagraphautospacing/)(bool) | Verwenden Sie festen [Paragraph](../../aspose.words/paragraph/) Abstand für die HTML-Autoeinstellung. |
| [set_DoNotUseIndentAsNumberingTabStop](./set_donotuseindentasnumberingtabstop/)(bool) | Ignorieren Sie hängenden Einzug beim Erstellen eines Tabstopps nach der Nummerierung. |
| [set_DoNotVertAlignCellWithSp](./set_donotvertaligncellwithsp/)(bool) | Richten Sie Zellen, die schwebende Objekte enthalten, nicht vertikal aus. |
| [set_DoNotVertAlignInTxbx](./set_donotvertalignintxbx/)(bool) | Ignorieren Sie die vertikale Ausrichtung in Textfeldern. |
| [set_DoNotWrapTextWithPunct](./set_donotwraptextwithpunct/)(bool) | Erlauben Sie hängende Interpunktion nicht mit dem Zeichenraster. |
| [set_FootnoteLayoutLikeWW8](./set_footnotelayoutlikeww8/)(bool) | Emulieren Sie die Fußnotenanordnung von Word 6.x/95/97. |
| [set_ForgetLastTabAlignment](./set_forgetlasttabalignment/)(bool) | Ignorieren Sie die Breite des letzten Tabstopps beim Ausrichten des [Paragraph](../../aspose.words/paragraph/), wenn er nicht linksbündig ist. |
| [set_GrowAutofit](./set_growautofit/)(bool) | Erlauben Sie, dass [Tables](../../aspose.words.tables/) automatisch in die Seitenränder passen. |
| [set_LayoutRawTableWidth](./set_layoutrawtablewidth/)(bool) | Ignorieren Sie den Abstand vor der Tabelle, wenn entschieden wird, ob die Tabelle ein schwebendes Objekt umbrechen soll. |
| [set_LayoutTableRowsApart](./set_layouttablerowsapart/)(bool) | Erlauben Sie, dass Tabellenzeilen [Inline](../../aspose.words/inline/) Objekte unabhängig umbrechen. |
| [set_LineWrapLikeWord6](./set_linewraplikeword6/)(bool) | Emulieren Sie den Zeilenumbruch von Word 6.0 für ostasiatischen Text. |
| [set_MWSmallCaps](./set_mwsmallcaps/)(bool) | Emulieren Sie Word 5.x für die Small-Caps-Formatierung auf dem Macintosh. |
| [set_NoColumnBalance](./set_nocolumnbalance/)(bool) | Balancieren Sie Textspalten innerhalb einer [Section](../../aspose.words/section/) nicht. |
| [set_NoExtraLineSpacing](./set_noextralinespacing/)(bool) | Zentrieren Sie Inhalte nicht auf Zeilen mit exakter Zeilenhöhe. |
| [set_NoLeading](./set_noleading/)(bool) | Fügen Sie keinen Zeilenabstand zwischen Textzeilen hinzu. |
| [set_NoSpaceRaiseLower](./set_nospaceraiselower/)(bool) | Vergrößern Sie die Zeilenhöhe nicht für hoch- oder tiefgestellten Text. |
| [set_NoTabHangInd](./set_notabhangind/)(bool) | Erstellen Sie keinen benutzerdefinierten Tabstopp für hängenden Einzug. |
| [set_OverrideTableStyleFontSizeAndJustification](./set_overridetablestylefontsizeandjustification/)(bool) | Gibt an, wie die Stilhierarchie des Dokuments ausgewertet wird. |
| [set_PrintBodyTextBeforeHeader](./set_printbodytextbeforeheader/)(bool) | Drucken Sie den [Body](../../aspose.words/body/) Text vor den Kopf-/Fußzeileninhalten. |
| [set_PrintColBlack](./set_printcolblack/)(bool) | Drucken Sie Farben als Schwarz‑Weiß ohne Dithering. |
| [set_SelectFldWithFirstOrLastChar](./set_selectfldwithfirstorlastchar/)(bool) | Wählen Sie das Feld aus, wenn das erste oder letzte Zeichen ausgewählt ist. |
| [set_ShapeLayoutLikeWW8](./set_shapelayoutlikeww8/)(bool) | Emulieren Sie den Textumbruch von Word 97 um schwebende Objekte. |
| [set_ShowBreaksInFrames](./set_showbreaksinframes/)(bool) | Zeigen Sie Seiten‑/Spaltenumbrüche an, die in Rahmen vorhanden sind. |
| [set_SpaceForUL](./set_spaceforul/)(bool) | Fügen Sie zusätzlichen Abstand unter der Grundlinie für unterstrichenen ostasiatischen Text hinzu. |
| [set_SpacingInWholePoints](./set_spacinginwholepoints/)(bool) | Erweitern/Kontrahieren Sie Text nur um ganze Punkte. |
| [set_SplitPgBreakAndParaMark](./set_splitpgbreakandparamark/)(bool) | Immer das [Paragraph](../../aspose.words/paragraph/) Mark auf die Seite nach einem Seitenumbruch verschieben. |
| [set_SubFontBySize](./set_subfontbysize/)(bool) | Priorität der [Font](../../aspose.words/font/) Größe während der [Font](../../aspose.words/font/) Substitution erhöhen. |
| [set_SuppressBottomSpacing](./set_suppressbottomspacing/)(bool) | Exakte Zeilenhöhe für die letzte Zeile auf der Seite ignorieren. |
| [set_SuppressSpacingAtTopOfPage](./set_suppressspacingattopofpage/)(bool) | Minimale Zeilenhöhe für die erste Zeile auf der Seite ignorieren. |
| [set_SuppressSpBfAfterPgBrk](./set_suppressspbfafterpgbrk/)(bool) | Kein Leerzeichen vor der ersten Zeile nach einem Seitenumbruch verwenden. |
| [set_SuppressTopSpacing](./set_suppresstopspacing/)(bool) | Minimale und exakte Zeilenhöhe für die erste Zeile auf der Seite ignorieren. |
| [set_SuppressTopSpacingWP](./set_suppresstopspacingwp/)(bool) | WordPerfect 5.x Zeilenabstand emulieren. |
| [set_SwapBordersFacingPgs](./set_swapbordersfacingpgs/)(bool) | [Paragraph](../../aspose.words/paragraph/) Rahmen auf ungeraden Seiten vertauschen. |
| [set_SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning](./set_swapinsideandoutsideformirrorindentsandrelativepositioning/)(bool) | Gibt an, innen und außen für Spiegel‑Einzüge und relative Positionierung zu vertauschen. |
| [set_TransparentMetafiles](./set_transparentmetafiles/)(bool) | Gibt an, den Bereich hinter Metadatei‑Bildern nicht zu leeren. |
| [set_TruncateFontHeightsLikeWP6](./set_truncatefontheightslikewp6/)(bool) | WordPerfect 6.x [Font](../../aspose.words/font/) Höhenberechnung emulieren. |
| [set_UICompat97To2003](./set_uicompat97to2003/)(bool) | Wahr, um UI‑Funktionalität zu deaktivieren, die nicht mit Word97-2003 kompatibel ist. Standardwert ist **false**. |
| [set_UlTrailSpace](./set_ultrailspace/)(bool) | Alle nachfolgenden Leerzeichen unterstreichen. |
| [set_UnderlineTabInNumList](./set_underlinetabinnumlist/)(bool) | Nachfolgendes Zeichen nach der Nummerierung unterstreichen. |
| [set_UseAltKinsokuLineBreakRules](./set_usealtkinsokulinebreakrules/)(bool) | Alternatives Set von Ostasiatischen Zeilenumbruch‑Regeln verwenden. |
| [set_UseAnsiKerningPairs](./set_useansikerningpairs/)(bool) | ANSI‑Kerning‑Paare aus [Fonts](../../aspose.words.fonts/) verwenden. |
| [set_UseFELayout](./set_usefelayout/)(bool) | Den Ostasiatisch/Komplex‑Skript [Layout](../../aspose.words.layout/) Code nicht umgehen. |
| [set_UseNormalStyleForList](./set_usenormalstyleforlist/)(bool) | Listen-[Paragraph](../../aspose.words/paragraph/)[Style](../../aspose.words/style/) nicht automatisch auf Aufzählungs‑/Nummerierungstext anwenden. |
| [set_UsePrinterMetrics](./set_useprintermetrics/)(bool) | Drucker‑Metriken verwenden, um Dokumente anzuzeigen. |
| [set_UseSingleBorderforContiguousCells](./set_usesingleborderforcontiguouscells/)(bool) | Vereinfachte Regeln für Tabellen-[Border](../../aspose.words/border/) Konflikte verwenden. |
| [set_UseWord2002TableStyleRules](./set_useword2002tablestylerules/)(bool) | Word 2002 Tabellen-[Style](../../aspose.words/style/) Regeln emulieren. |
| [set_UseWord2010TableStyleRules](./set_useword2010tablestylerules/)(bool) | Gibt an, Word2010 Tabellen‑Stilregeln zu verwenden. |
| [set_UseWord97LineBreakRules](./set_useword97linebreakrules/)(bool) | Word 97 Ostasiatischen Zeilenumbruch emulieren. |
| [set_WPJustification](./set_wpjustification/)(bool) | WordPerfect 6.x [Paragraph](../../aspose.words/paragraph/) Blocksatz emulieren. |
| [set_WPSpaceWidth](./set_wpspacewidth/)(bool) | Gibt an, ob die Breite eines Leerzeichens wie in WordPerfect 5.x festgelegt werden soll. |
| [set_WrapTrailSpaces](./set_wraptrailspaces/)(bool) | Zeilenumbruch nachfolgenden Leerzeichen. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man eine OOXML‑Compliance‑Spezifikation für ein gespeichertes Dokument festlegt, an die es sich halten muss.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Wenn wir Kompatibilitätsoptionen so konfigurieren, dass sie mit Microsoft Word 2003 konform sind,
// Das Einfügen eines Bildes definiert seine Form mithilfe von VML.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2003);
builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Vml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());

// Der "ISO/IEC 29500:2008" OOXML‑Standard unterstützt keine VML‑Formen.
// Wenn wir die "Compliance"‑Eigenschaft des SaveOptions‑Objekts auf "OoxmlCompliance.Iso29500_2008_Strict" setzen,
// muss jedes Dokument, das wir beim Übergeben dieses Objekts speichern, diesem Standard folgen.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docx);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Unser gespeichertes Dokument definiert die Form mithilfe von DML, um dem "ISO/IEC 29500:2008" OOXML‑Standard zu entsprechen.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Iso29500Strict.docx");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_MarkupLanguage());
```


Zeigt, wie der Textinhalt einer Textbox vertikal ausgerichtet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Top", um
// den Text in dieser Textbox mit der oberen Seite der Form auszurichten.
// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Middle", um
// den Text in dieser Textbox in der Mitte der Form auszurichten.
// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Bottom", um
// den Text in dieser Textbox an der Unterseite der Form auszurichten.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Die vertikale Ausrichtung von Text in Textboxen ist ab Microsoft Word 2007 verfügbar.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
