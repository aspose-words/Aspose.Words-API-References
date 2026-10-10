---
title: "Kompatibilität"
linktitle: "Kompatibilität"
second_title: "Aspose.Words für Java"
description: "Gibt die Namen von Kompatibilitätsoptionen in Java an."
type: docs
weight: 119
url: /de/java/com.aspose.words/compatibility/
---

**Inheritance:**
java.lang.Object
```
public class Compatibility
```

Gibt die Namen der Kompatibilitätsoptionen an.

 **Examples:** 

Zeigt, wie das Dokument für verschiedene Versionen von Microsoft Word optimiert werden kann.

```

 public void optimizeFor() throws Exception
 {
     Document doc = new Document();

     // This object contains an extensive list of flags unique to each document
     // that allow us to facilitate backward compatibility with older versions of Microsoft Word.
     CompatibilityOptions options = doc.getCompatibilityOptions();

     // Print the default settings for a blank document.
     System.out.println("\nDefault optimization settings:");
     printCompatibilityOptions(options);

     // We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
     doc.save(getArtifactsDir() + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

     // We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
     doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2010);
     System.out.println("\nOptimized for Word 2010:");
     printCompatibilityOptions(options);

     doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2000);
     System.out.println("\nOptimized for Word 2000:");
     printCompatibilityOptions(options);
 }

 /// 
 /// Groups all flags in a document's compatibility options object by state, then prints each group.
 /// 
 private static void printCompatibilityOptions(CompatibilityOptions options)
 {
     ArrayList enabledOptions = new ArrayList();
     ArrayList disabledOptions = new ArrayList();
     addOptionName(options.getAdjustLineHeightInTable(), "AdjustLineHeightInTable", enabledOptions, disabledOptions);
     addOptionName(options.getAlignTablesRowByRow(), "AlignTablesRowByRow", enabledOptions, disabledOptions);
     addOptionName(options.getAllowSpaceOfSameStyleInTable(), "AllowSpaceOfSameStyleInTable", enabledOptions, disabledOptions);
     addOptionName(options.getApplyBreakingRules(), "ApplyBreakingRules", enabledOptions, disabledOptions);
     addOptionName(options.getAutoSpaceLikeWord95(), "AutoSpaceLikeWord95", enabledOptions, disabledOptions);
     addOptionName(options.getAutofitToFirstFixedWidthCell(), "AutofitToFirstFixedWidthCell", enabledOptions, disabledOptions);
     addOptionName(options.getBalanceSingleByteDoubleByteWidth(), "BalanceSingleByteDoubleByteWidth", enabledOptions, disabledOptions);
     addOptionName(options.getCachedColBalance(), "CachedColBalance", enabledOptions, disabledOptions);
     addOptionName(options.getConvMailMergeEsc(), "ConvMailMergeEsc", enabledOptions, disabledOptions);
     addOptionName(options.getDisableOpenTypeFontFormattingFeatures(), "DisableOpenTypeFontFormattingFeatures", enabledOptions, disabledOptions);
     addOptionName(options.getDisplayHangulFixedWidth(), "DisplayHangulFixedWidth", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotAutofitConstrainedTables(), "DoNotAutofitConstrainedTables", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotBreakConstrainedForcedTable(), "DoNotBreakConstrainedForcedTable", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotBreakWrappedTables(), "DoNotBreakWrappedTables", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotExpandShiftReturn(), "DoNotExpandShiftReturn", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotLeaveBackslashAlone(), "DoNotLeaveBackslashAlone", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotSnapToGridInCell(), "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotSuppressIndentation(), "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotSuppressParagraphBorders(), "DoNotSuppressParagraphBorders", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotUseEastAsianBreakRules(), "DoNotUseEastAsianBreakRules", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotUseHTMLParagraphAutoSpacing(), "DoNotUseHTMLParagraphAutoSpacing", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotUseIndentAsNumberingTabStop(), "DoNotUseIndentAsNumberingTabStop", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotVertAlignCellWithSp(), "DoNotVertAlignCellWithSp", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotVertAlignInTxbx(), "DoNotVertAlignInTxbx", enabledOptions, disabledOptions);
     addOptionName(options.getDoNotWrapTextWithPunct(), "DoNotWrapTextWithPunct", enabledOptions, disabledOptions);
     addOptionName(options.getFootnoteLayoutLikeWW8(), "FootnoteLayoutLikeWW8", enabledOptions, disabledOptions);
     addOptionName(options.getForgetLastTabAlignment(), "ForgetLastTabAlignment", enabledOptions, disabledOptions);
     addOptionName(options.getGrowAutofit(), "GrowAutofit", enabledOptions, disabledOptions);
     addOptionName(options.getLayoutRawTableWidth(), "LayoutRawTableWidth", enabledOptions, disabledOptions);
     addOptionName(options.getLayoutTableRowsApart(), "LayoutTableRowsApart", enabledOptions, disabledOptions);
     addOptionName(options.getLineWrapLikeWord6(), "LineWrapLikeWord6", enabledOptions, disabledOptions);
     addOptionName(options.getMWSmallCaps(), "MWSmallCaps", enabledOptions, disabledOptions);
     addOptionName(options.getNoColumnBalance(), "NoColumnBalance", enabledOptions, disabledOptions);
     addOptionName(options.getNoExtraLineSpacing(), "NoExtraLineSpacing", enabledOptions, disabledOptions);
     addOptionName(options.getNoLeading(), "NoLeading", enabledOptions, disabledOptions);
     addOptionName(options.getNoSpaceRaiseLower(), "NoSpaceRaiseLower", enabledOptions, disabledOptions);
     addOptionName(options.getNoTabHangInd(), "NoTabHangInd", enabledOptions, disabledOptions);
     addOptionName(options.getOverrideTableStyleFontSizeAndJustification(), "OverrideTableStyleFontSizeAndJustification", enabledOptions, disabledOptions);
     addOptionName(options.getPrintBodyTextBeforeHeader(), "PrintBodyTextBeforeHeader", enabledOptions, disabledOptions);
     addOptionName(options.getPrintColBlack(), "PrintColBlack", enabledOptions, disabledOptions);
     addOptionName(options.getSelectFldWithFirstOrLastChar(), "SelectFldWithFirstOrLastChar", enabledOptions, disabledOptions);
     addOptionName(options.getShapeLayoutLikeWW8(), "ShapeLayoutLikeWW8", enabledOptions, disabledOptions);
     addOptionName(options.getShowBreaksInFrames(), "ShowBreaksInFrames", enabledOptions, disabledOptions);
     addOptionName(options.getSpaceForUL(), "SpaceForUL", enabledOptions, disabledOptions);
     addOptionName(options.getSpacingInWholePoints(), "SpacingInWholePoints", enabledOptions, disabledOptions);
     addOptionName(options.getSplitPgBreakAndParaMark(), "SplitPgBreakAndParaMark", enabledOptions, disabledOptions);
     addOptionName(options.getSubFontBySize(), "SubFontBySize", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressBottomSpacing(), "SuppressBottomSpacing", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressSpBfAfterPgBrk(), "SuppressSpBfAfterPgBrk", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressSpacingAtTopOfPage(), "SuppressSpacingAtTopOfPage", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressTopSpacing(), "SuppressTopSpacing", enabledOptions, disabledOptions);
     addOptionName(options.getSuppressTopSpacingWP(), "SuppressTopSpacingWP", enabledOptions, disabledOptions);
     addOptionName(options.getSwapBordersFacingPgs(), "SwapBordersFacingPgs", enabledOptions, disabledOptions);
     addOptionName(options.getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(), "SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning", enabledOptions, disabledOptions);
     addOptionName(options.getTransparentMetafiles(), "TransparentMetafiles", enabledOptions, disabledOptions);
     addOptionName(options.getTruncateFontHeightsLikeWP6(), "TruncateFontHeightsLikeWP6", enabledOptions, disabledOptions);
     addOptionName(options.getUICompat97To2003(), "UICompat97To2003", enabledOptions, disabledOptions);
     addOptionName(options.getUlTrailSpace(), "UlTrailSpace", enabledOptions, disabledOptions);
     addOptionName(options.getUnderlineTabInNumList(), "UnderlineTabInNumList", enabledOptions, disabledOptions);
     addOptionName(options.getUseAltKinsokuLineBreakRules(), "UseAltKinsokuLineBreakRules", enabledOptions, disabledOptions);
     addOptionName(options.getUseAnsiKerningPairs(), "UseAnsiKerningPairs", enabledOptions, disabledOptions);
     addOptionName(options.getUseFELayout(), "UseFELayout", enabledOptions, disabledOptions);
     addOptionName(options.getUseNormalStyleForList(), "UseNormalStyleForList", enabledOptions, disabledOptions);
     addOptionName(options.getUsePrinterMetrics(), "UsePrinterMetrics", enabledOptions, disabledOptions);
     addOptionName(options.getUseSingleBorderforContiguousCells(), "UseSingleBorderforContiguousCells", enabledOptions, disabledOptions);
     addOptionName(options.getUseWord2002TableStyleRules(), "UseWord2002TableStyleRules", enabledOptions, disabledOptions);
     addOptionName(options.getUseWord2010TableStyleRules(), "UseWord2010TableStyleRules", enabledOptions, disabledOptions);
     addOptionName(options.getUseWord97LineBreakRules(), "UseWord97LineBreakRules", enabledOptions, disabledOptions);
     addOptionName(options.getWPJustification(), "WPJustification", enabledOptions, disabledOptions);
     addOptionName(options.getWPSpaceWidth(), "WPSpaceWidth", enabledOptions, disabledOptions);
     addOptionName(options.getWrapTrailSpaces(), "WrapTrailSpaces", enabledOptions, disabledOptions);
     System.out.println("\tEnabled options:");
     for (String optionName : enabledOptions)
         System.out.println("\t\t{optionName}");
     System.out.println("\tDisabled options:");
     for (String optionName : disabledOptions)
         System.out.println("\t\t{optionName}");
 }

 private static void addOptionName(boolean option, String optionName, ArrayList enabledOptions, ArrayList disabledOptions)
 {
     if (option)
         enabledOptions.add(optionName);
     else
         disabledOptions.add(optionName);
 }
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ADJUST_LINE_HEIGHT_IN_TABLE](#ADJUST-LINE-HEIGHT-IN-TABLE) | Zeilenhöhe in Tabelle anpassen |
| [ALIGN_TABLE_ROW_BY_ROW](#ALIGN-TABLE-ROW-BY-ROW) | Tabellenzeilen nach Regel ausrichten |
| [ALLOW_SPACE_OF_SAME_STYLE_IN_TABLE](#ALLOW-SPACE-OF-SAME-STYLE-IN-TABLE) | Leerzeichen desselben Stils in Tabelle zulassen |
| [APPLY_BREAKING_RULES](#APPLY-BREAKING-RULES) | Umbruchregeln anwenden |
| [AUTOFIT_TO_FIRST_FIXED_WIDTH_CELL](#AUTOFIT-TO-FIRST-FIXED-WIDTH-CELL) | AutoFit auf die erste Zelle mit fester Breite |
| [AUTO_SPACE_LIKE_WORD_95](#AUTO-SPACE-LIKE-WORD-95) | Automatischer Abstand wie Word 95 |
| [BALANCE_SINGLE_BYTE_DOUBLE_BYTE_WIDTH](#BALANCE-SINGLE-BYTE-DOUBLE-BYTE-WIDTH) | Einzelbyte- und Doppelbyte-Breiten ausbalancieren |
| [CACHED_COL_BALANCE](#CACHED-COL-BALANCE) | Zwischengespeichertes Spaltenausbalancieren |
| [CONV_MAIL_MERGE_ESC](#CONV-MAIL-MERGE-ESC) | Mail-Merge-Fluchtzeichen konvertieren |
| [DISABLE_OPEN_TYPE_FONT_FORMATTING_FEATURES](#DISABLE-OPEN-TYPE-FONT-FORMATTING-FEATURES) | OpenType-Schriftformatierungsfunktionen deaktivieren |
| [DISPLAY_HANGUL_FIXED_WIDTH](#DISPLAY-HANGUL-FIXED-WIDTH) | Hangul mit fester Breite anzeigen |
| [DO_NOT_AUTOFIT_CONSTRAINED_TABLES](#DO-NOT-AUTOFIT-CONSTRAINED-TABLES) | Keine AutoFit für eingeschränkte Tabellen |
| [DO_NOT_BREAK_CONSTRAINED_FORCED_TABLE](#DO-NOT-BREAK-CONSTRAINED-FORCED-TABLE) | Eingeschränkte erzwungene Tabellen nicht umbrechen |
| [DO_NOT_BREAK_WRAPPED_TABLES](#DO-NOT-BREAK-WRAPPED-TABLES) | Umgebrochene Tabellen nicht umbrechen |
| [DO_NOT_EXPAND_ON_SHIFT_RETURN](#DO-NOT-EXPAND-ON-SHIFT-RETURN) | Bei Shift+Return nicht erweitern |
| [DO_NOT_LEAVE_BACKSLASH_ALONE](#DO-NOT-LEAVE-BACKSLASH-ALONE) | Lassen Sie den Backslash nicht allein |
| [DO_NOT_SNAP_TO_GRID_IN_CELL](#DO-NOT-SNAP-TO-GRID-IN-CELL) | Richten Sie Zellen nicht am Raster aus |
| [DO_NOT_SUPPRESS_INDENTATION](#DO-NOT-SUPPRESS-INDENTATION) | Unterdrücken Sie die Einrückung nicht |
| [DO_NOT_SUPPRESS_PARAGRAPH_BORDER](#DO-NOT-SUPPRESS-PARAGRAPH-BORDER) | Unterdrücken Sie den Absatzrahmen nicht |
| [DO_NOT_USE_EAST_ASIAN_BREAK_RULES](#DO-NOT-USE-EAST-ASIAN-BREAK-RULES) | Verwenden Sie keine ostasiatischen Umbruchregeln |
| [DO_NOT_USE_HTML_PARAGRAPH_AUTO_SPACING](#DO-NOT-USE-HTML-PARAGRAPH-AUTO-SPACING) | Verwenden Sie kein automatisches HTML-Absatzabstand |
| [DO_NOT_USE_INDENT_AS_NUMBERING_TAB_STOP](#DO-NOT-USE-INDENT-AS-NUMBERING-TAB-STOP) | Verwenden Sie Einzug nicht als Nummerierungs-Tabulator |
| [DO_NOT_VERT_ALIGN_CELL_WITH_SP](#DO-NOT-VERT-ALIGN-CELL-WITH-SP) | Richten Sie Zellen nicht vertikal mit Abstand aus |
| [DO_NOT_VERT_ALIGN_IN_TXBX](#DO-NOT-VERT-ALIGN-IN-TXBX) | Richten Sie Textfelder nicht vertikal aus |
| [DO_NOT_WRAP_TEXT_WITH_PUNCT](#DO-NOT-WRAP-TEXT-WITH-PUNCT) | Zeilenumbruch bei Satzzeichen nicht zulassen |
| [FOOTNOTE_LAYOUT_LIKE_WW_8](#FOOTNOTE-LAYOUT-LIKE-WW-8) | Fußnotenlayout wie Word 2000 |
| [FORGET_LAST_TAB_ALIGNMENT](#FORGET-LAST-TAB-ALIGNMENT) | Letzte Tab-Ausrichtung vergessen |
| [GROW_AUTOFIT](#GROW-AUTOFIT) | AutoFit vergrößern |
| [LAYOUT_RAW_TABLE_WIDTH](#LAYOUT-RAW-TABLE-WIDTH) | Rohbreite der Tabelle layouten |
| [LAYOUT_TABLE_ROWS_APART](#LAYOUT-TABLE-ROWS-APART) | Tabellenzeilen auseinander layouten |
| [LINE_WRAP_LIKE_WORD_6](#LINE-WRAP-LIKE-WORD-6) | Zeilenumbruch wie Word 6 |
| [MW_SMALL_CAPS](#MW-SMALL-CAPS) |  |
| [NO_COLUMN_BALANCE](#NO-COLUMN-BALANCE) | Keine Spaltenausbalancierung |
| [NO_EXTRA_LINE_SPACING](#NO-EXTRA-LINE-SPACING) | Kein zusätzlicher Zeilenabstand |
| [NO_LEADING](#NO-LEADING) | Kein Zeilenabstand |
| [NO_SPACE_RAISE_LOWER](#NO-SPACE-RAISE-LOWER) | Kein Abstand erhöhen/senken |
| [NO_TAB_HANG_IND](#NO-TAB-HANG-IND) | Kein hängender Tab-Einzug |
| [OVERRIDE_TABLE_STYLE_FONT_SIZE_AND_JUSTIFICATION](#OVERRIDE-TABLE-STYLE-FONT-SIZE-AND-JUSTIFICATION) | Tabellenstil-Schriftgröße und -Ausrichtung überschreiben |
| [PRINT_BODY_TEXT_BEFORE_HEADER](#PRINT-BODY-TEXT-BEFORE-HEADER) | Fließtext vor Kopfzeile drucken |
| [PRINT_COL_BLACK](#PRINT-COL-BLACK) | Spaltenhintergrund drucken |
| [SELECT_FLD_WITH_FIRST_OR_LAST_CHAR](#SELECT-FLD-WITH-FIRST-OR-LAST-CHAR) | Feld mit erstem oder letztem Zeichen auswählen |
| [SHAPE_LAYOUT_LIKE_WW_8](#SHAPE-LAYOUT-LIKE-WW-8) | Formlayout wie Word 2000 |
| [SHOW_BREAKS_IN_FRAMES](#SHOW-BREAKS-IN-FRAMES) | Umbrüche in Rahmen anzeigen |
| [SPACE_FOR_UL](#SPACE-FOR-UL) | Platz für Unterstreichung |
| [SPACING_IN_WHOLE_POINTS](#SPACING-IN-WHOLE-POINTS) | Abstand in ganzen Punkten |
| [SPLIT_PG_BREAK_AND_PARA_MARK](#SPLIT-PG-BREAK-AND-PARA-MARK) | Seitenumbruch und Absatzmarke trennen |
| [SUB_FONT_BY_SIZE](#SUB-FONT-BY-SIZE) | Schriftart nach Größe ersetzen |
| [SUPPRESS_BOTTOM_SPACING](#SUPPRESS-BOTTOM-SPACING) | Untere Abstände unterdrücken |
| [SUPPRESS_SP_BF_AFTER_PG_BRK](#SUPPRESS-SP-BF-AFTER-PG-BRK) | Leerzeichen vor Absatzumbruch unterdrücken |
| [SUPPRESS_TOP_LINE_SPACING_WP](#SUPPRESS-TOP-LINE-SPACING-WP) | Zeilenabstand oben in WordPerfect unterdrücken |
| [SUPPRESS_TOP_SPACING](#SUPPRESS-TOP-SPACING) | Oberen Abstand unterdrücken |
| [SUPPRESS_TOP_SPACING_AT_TOP_OF_PAGE](#SUPPRESS-TOP-SPACING-AT-TOP-OF-PAGE) | Zeilenabstand oben in WordPerfect unterdrücken |
| [SWAP_BORDERS_ODD_FACING_PGS](#SWAP-BORDERS-ODD-FACING-PGS) | Ränder auf ungeraden Seiten vertauschen |
| [SWAP_INSIDE_AND_OUTSIDE_FOR_MIRROR_INDENTS_AND_RELATIVE_POSITIONING](#SWAP-INSIDE-AND-OUTSIDE-FOR-MIRROR-INDENTS-AND-RELATIVE-POSITIONING) | Innen- und Außenränder für Spiegel‑Einzüge und relative Positionierung vertauschen |
| [TRANSPARENT_METAFILES](#TRANSPARENT-METAFILES) | Transparente Metadateien |
| [TRUNCATE_FONT_HEIGHT_LIKE_WP_6](#TRUNCATE-FONT-HEIGHT-LIKE-WP-6) | Schrifthöhe wie WordPerfect 6 kürzen |
| [UI_COMPAT_97_TO_2003](#UI-COMPAT-97-TO-2003) |  |
| [UL_TRAIL_SPACE](#UL-TRAIL-SPACE) | Nachgestelltes Leerzeichen unterstreichen |
| [UNDERLINE_TAB_IN_NUM_LIST](#UNDERLINE-TAB-IN-NUM-LIST) | Tabulator in nummerierter Liste unterstreichen |
| [USE_ALT_KINSOKU_LINE_BREAK_RULES](#USE-ALT-KINSOKU-LINE-BREAK-RULES) | Alt‑Kinsoku‑Zeilenumbruchregeln verwenden |
| [USE_ANSI_KERNING_PAIRS](#USE-ANSI-KERNING-PAIRS) | ANSI‑Kerning‑Paare verwenden |
| [USE_FE_LAYOUT](#USE-FE-LAYOUT) |  |
| [USE_NORMAL_STYLE_FOR_LIST](#USE-NORMAL-STYLE-FOR-LIST) | Normal‑Format für Liste verwenden |
| [USE_PRINTER_METRICS](#USE-PRINTER-METRICS) | Drucker‑Metriken verwenden |
| [USE_SINGLE_BORDERFOR_CONTIGUOUS_CELLS](#USE-SINGLE-BORDERFOR-CONTIGUOUS-CELLS) | Einzelnen Rand für zusammenhängende Zellen verwenden |
| [USE_WORD_2002_TABLE_STYLE_RULES](#USE-WORD-2002-TABLE-STYLE-RULES) | Word‑2002‑Tabellenformatregeln verwenden |
| [USE_WORD_2010_TABLE_STYLE_RULES](#USE-WORD-2010-TABLE-STYLE-RULES) | Word‑2010‑Tabellenformatregeln verwenden |
| [USE_WORD_97_LINE_BREAK_RULES](#USE-WORD-97-LINE-BREAK-RULES) | Word‑97‑Zeilenumbruchregeln verwenden |
| [WP_JUSTIFICATION](#WP-JUSTIFICATION) |  |
| [WP_SPACE_WIDTH](#WP-SPACE-WIDTH) |  |
| [WRAP_TRAIL_SPACES](#WRAP-TRAIL-SPACES) | Nachgestellte Leerzeichen umbrechen |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String compatibilityName)](#fromName-java.lang.String) |  |
| [getName(int compatibility)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compatibility)](#toString-int) |  |
### ADJUST_LINE_HEIGHT_IN_TABLE {#ADJUST-LINE-HEIGHT-IN-TABLE}
```
public static int ADJUST_LINE_HEIGHT_IN_TABLE
```


Zeilenhöhe in Tabelle anpassen

### ALIGN_TABLE_ROW_BY_ROW {#ALIGN-TABLE-ROW-BY-ROW}
```
public static int ALIGN_TABLE_ROW_BY_ROW
```


Tabellenzeilen nach Regel ausrichten

### ALLOW_SPACE_OF_SAME_STYLE_IN_TABLE {#ALLOW-SPACE-OF-SAME-STYLE-IN-TABLE}
```
public static int ALLOW_SPACE_OF_SAME_STYLE_IN_TABLE
```


Leerzeichen desselben Stils in Tabelle zulassen

### APPLY_BREAKING_RULES {#APPLY-BREAKING-RULES}
```
public static int APPLY_BREAKING_RULES
```


Umbruchregeln anwenden

### AUTOFIT_TO_FIRST_FIXED_WIDTH_CELL {#AUTOFIT-TO-FIRST-FIXED-WIDTH-CELL}
```
public static int AUTOFIT_TO_FIRST_FIXED_WIDTH_CELL
```


AutoFit auf die erste Zelle mit fester Breite

### AUTO_SPACE_LIKE_WORD_95 {#AUTO-SPACE-LIKE-WORD-95}
```
public static int AUTO_SPACE_LIKE_WORD_95
```


Automatischer Abstand wie Word 95

### BALANCE_SINGLE_BYTE_DOUBLE_BYTE_WIDTH {#BALANCE-SINGLE-BYTE-DOUBLE-BYTE-WIDTH}
```
public static int BALANCE_SINGLE_BYTE_DOUBLE_BYTE_WIDTH
```


Einzelbyte- und Doppelbyte-Breiten ausbalancieren

### CACHED_COL_BALANCE {#CACHED-COL-BALANCE}
```
public static int CACHED_COL_BALANCE
```


Zwischengespeichertes Spaltenausbalancieren

### CONV_MAIL_MERGE_ESC {#CONV-MAIL-MERGE-ESC}
```
public static int CONV_MAIL_MERGE_ESC
```


Mail-Merge-Fluchtzeichen konvertieren

### DISABLE_OPEN_TYPE_FONT_FORMATTING_FEATURES {#DISABLE-OPEN-TYPE-FONT-FORMATTING-FEATURES}
```
public static int DISABLE_OPEN_TYPE_FONT_FORMATTING_FEATURES
```


OpenType-Schriftformatierungsfunktionen deaktivieren

### DISPLAY_HANGUL_FIXED_WIDTH {#DISPLAY-HANGUL-FIXED-WIDTH}
```
public static int DISPLAY_HANGUL_FIXED_WIDTH
```


Hangul mit fester Breite anzeigen

### DO_NOT_AUTOFIT_CONSTRAINED_TABLES {#DO-NOT-AUTOFIT-CONSTRAINED-TABLES}
```
public static int DO_NOT_AUTOFIT_CONSTRAINED_TABLES
```


Keine AutoFit für eingeschränkte Tabellen

### DO_NOT_BREAK_CONSTRAINED_FORCED_TABLE {#DO-NOT-BREAK-CONSTRAINED-FORCED-TABLE}
```
public static int DO_NOT_BREAK_CONSTRAINED_FORCED_TABLE
```


Eingeschränkte erzwungene Tabellen nicht umbrechen

### DO_NOT_BREAK_WRAPPED_TABLES {#DO-NOT-BREAK-WRAPPED-TABLES}
```
public static int DO_NOT_BREAK_WRAPPED_TABLES
```


Umgebrochene Tabellen nicht umbrechen

### DO_NOT_EXPAND_ON_SHIFT_RETURN {#DO-NOT-EXPAND-ON-SHIFT-RETURN}
```
public static int DO_NOT_EXPAND_ON_SHIFT_RETURN
```


Bei Shift+Return nicht erweitern

### DO_NOT_LEAVE_BACKSLASH_ALONE {#DO-NOT-LEAVE-BACKSLASH-ALONE}
```
public static int DO_NOT_LEAVE_BACKSLASH_ALONE
```


Lassen Sie den Backslash nicht allein

### DO_NOT_SNAP_TO_GRID_IN_CELL {#DO-NOT-SNAP-TO-GRID-IN-CELL}
```
public static int DO_NOT_SNAP_TO_GRID_IN_CELL
```


Richten Sie Zellen nicht am Raster aus

### DO_NOT_SUPPRESS_INDENTATION {#DO-NOT-SUPPRESS-INDENTATION}
```
public static int DO_NOT_SUPPRESS_INDENTATION
```


Unterdrücken Sie die Einrückung nicht

### DO_NOT_SUPPRESS_PARAGRAPH_BORDER {#DO-NOT-SUPPRESS-PARAGRAPH-BORDER}
```
public static int DO_NOT_SUPPRESS_PARAGRAPH_BORDER
```


Unterdrücken Sie den Absatzrahmen nicht

### DO_NOT_USE_EAST_ASIAN_BREAK_RULES {#DO-NOT-USE-EAST-ASIAN-BREAK-RULES}
```
public static int DO_NOT_USE_EAST_ASIAN_BREAK_RULES
```


Verwenden Sie keine ostasiatischen Umbruchregeln

### DO_NOT_USE_HTML_PARAGRAPH_AUTO_SPACING {#DO-NOT-USE-HTML-PARAGRAPH-AUTO-SPACING}
```
public static int DO_NOT_USE_HTML_PARAGRAPH_AUTO_SPACING
```


Verwenden Sie kein automatisches HTML-Absatzabstand

### DO_NOT_USE_INDENT_AS_NUMBERING_TAB_STOP {#DO-NOT-USE-INDENT-AS-NUMBERING-TAB-STOP}
```
public static int DO_NOT_USE_INDENT_AS_NUMBERING_TAB_STOP
```


Verwenden Sie Einzug nicht als Nummerierungs-Tabulator

### DO_NOT_VERT_ALIGN_CELL_WITH_SP {#DO-NOT-VERT-ALIGN-CELL-WITH-SP}
```
public static int DO_NOT_VERT_ALIGN_CELL_WITH_SP
```


Richten Sie Zellen nicht vertikal mit Abstand aus

### DO_NOT_VERT_ALIGN_IN_TXBX {#DO-NOT-VERT-ALIGN-IN-TXBX}
```
public static int DO_NOT_VERT_ALIGN_IN_TXBX
```


Richten Sie Textfelder nicht vertikal aus

### DO_NOT_WRAP_TEXT_WITH_PUNCT {#DO-NOT-WRAP-TEXT-WITH-PUNCT}
```
public static int DO_NOT_WRAP_TEXT_WITH_PUNCT
```


Zeilenumbruch bei Satzzeichen nicht zulassen

### FOOTNOTE_LAYOUT_LIKE_WW_8 {#FOOTNOTE-LAYOUT-LIKE-WW-8}
```
public static int FOOTNOTE_LAYOUT_LIKE_WW_8
```


Fußnotenlayout wie Word 2000

### FORGET_LAST_TAB_ALIGNMENT {#FORGET-LAST-TAB-ALIGNMENT}
```
public static int FORGET_LAST_TAB_ALIGNMENT
```


Letzte Tab-Ausrichtung vergessen

### GROW_AUTOFIT {#GROW-AUTOFIT}
```
public static int GROW_AUTOFIT
```


AutoFit vergrößern

### LAYOUT_RAW_TABLE_WIDTH {#LAYOUT-RAW-TABLE-WIDTH}
```
public static int LAYOUT_RAW_TABLE_WIDTH
```


Rohbreite der Tabelle layouten

### LAYOUT_TABLE_ROWS_APART {#LAYOUT-TABLE-ROWS-APART}
```
public static int LAYOUT_TABLE_ROWS_APART
```


Tabellenzeilen auseinander layouten

### LINE_WRAP_LIKE_WORD_6 {#LINE-WRAP-LIKE-WORD-6}
```
public static int LINE_WRAP_LIKE_WORD_6
```


Zeilenumbruch wie Word 6

### MW_SMALL_CAPS {#MW-SMALL-CAPS}
```
public static int MW_SMALL_CAPS
```


### NO_COLUMN_BALANCE {#NO-COLUMN-BALANCE}
```
public static int NO_COLUMN_BALANCE
```


Keine Spaltenausbalancierung

### NO_EXTRA_LINE_SPACING {#NO-EXTRA-LINE-SPACING}
```
public static int NO_EXTRA_LINE_SPACING
```


Kein zusätzlicher Zeilenabstand

### NO_LEADING {#NO-LEADING}
```
public static int NO_LEADING
```


Kein Zeilenabstand

### NO_SPACE_RAISE_LOWER {#NO-SPACE-RAISE-LOWER}
```
public static int NO_SPACE_RAISE_LOWER
```


Kein Abstand erhöhen/senken

### NO_TAB_HANG_IND {#NO-TAB-HANG-IND}
```
public static int NO_TAB_HANG_IND
```


Kein hängender Tab-Einzug

### OVERRIDE_TABLE_STYLE_FONT_SIZE_AND_JUSTIFICATION {#OVERRIDE-TABLE-STYLE-FONT-SIZE-AND-JUSTIFICATION}
```
public static int OVERRIDE_TABLE_STYLE_FONT_SIZE_AND_JUSTIFICATION
```


Tabellenstil-Schriftgröße und -Ausrichtung überschreiben

### PRINT_BODY_TEXT_BEFORE_HEADER {#PRINT-BODY-TEXT-BEFORE-HEADER}
```
public static int PRINT_BODY_TEXT_BEFORE_HEADER
```


Fließtext vor Kopfzeile drucken

### PRINT_COL_BLACK {#PRINT-COL-BLACK}
```
public static int PRINT_COL_BLACK
```


Spaltenhintergrund drucken

### SELECT_FLD_WITH_FIRST_OR_LAST_CHAR {#SELECT-FLD-WITH-FIRST-OR-LAST-CHAR}
```
public static int SELECT_FLD_WITH_FIRST_OR_LAST_CHAR
```


Feld mit erstem oder letztem Zeichen auswählen

### SHAPE_LAYOUT_LIKE_WW_8 {#SHAPE-LAYOUT-LIKE-WW-8}
```
public static int SHAPE_LAYOUT_LIKE_WW_8
```


Formlayout wie Word 2000

### SHOW_BREAKS_IN_FRAMES {#SHOW-BREAKS-IN-FRAMES}
```
public static int SHOW_BREAKS_IN_FRAMES
```


Umbrüche in Rahmen anzeigen

### SPACE_FOR_UL {#SPACE-FOR-UL}
```
public static int SPACE_FOR_UL
```


Platz für Unterstreichung

### SPACING_IN_WHOLE_POINTS {#SPACING-IN-WHOLE-POINTS}
```
public static int SPACING_IN_WHOLE_POINTS
```


Abstand in ganzen Punkten

### SPLIT_PG_BREAK_AND_PARA_MARK {#SPLIT-PG-BREAK-AND-PARA-MARK}
```
public static int SPLIT_PG_BREAK_AND_PARA_MARK
```


Seitenumbruch und Absatzmarke trennen

### SUB_FONT_BY_SIZE {#SUB-FONT-BY-SIZE}
```
public static int SUB_FONT_BY_SIZE
```


Schriftart nach Größe ersetzen

### SUPPRESS_BOTTOM_SPACING {#SUPPRESS-BOTTOM-SPACING}
```
public static int SUPPRESS_BOTTOM_SPACING
```


Untere Abstände unterdrücken

### SUPPRESS_SP_BF_AFTER_PG_BRK {#SUPPRESS-SP-BF-AFTER-PG-BRK}
```
public static int SUPPRESS_SP_BF_AFTER_PG_BRK
```


Leerzeichen vor Absatzumbruch unterdrücken

### SUPPRESS_TOP_LINE_SPACING_WP {#SUPPRESS-TOP-LINE-SPACING-WP}
```
public static int SUPPRESS_TOP_LINE_SPACING_WP
```


Zeilenabstand oben in WordPerfect unterdrücken

### SUPPRESS_TOP_SPACING {#SUPPRESS-TOP-SPACING}
```
public static int SUPPRESS_TOP_SPACING
```


Oberen Abstand unterdrücken

### SUPPRESS_TOP_SPACING_AT_TOP_OF_PAGE {#SUPPRESS-TOP-SPACING-AT-TOP-OF-PAGE}
```
public static int SUPPRESS_TOP_SPACING_AT_TOP_OF_PAGE
```


Zeilenabstand oben in WordPerfect unterdrücken

### SWAP_BORDERS_ODD_FACING_PGS {#SWAP-BORDERS-ODD-FACING-PGS}
```
public static int SWAP_BORDERS_ODD_FACING_PGS
```


Ränder auf ungeraden Seiten vertauschen

### SWAP_INSIDE_AND_OUTSIDE_FOR_MIRROR_INDENTS_AND_RELATIVE_POSITIONING {#SWAP-INSIDE-AND-OUTSIDE-FOR-MIRROR-INDENTS-AND-RELATIVE-POSITIONING}
```
public static int SWAP_INSIDE_AND_OUTSIDE_FOR_MIRROR_INDENTS_AND_RELATIVE_POSITIONING
```


Innen- und Außenränder für Spiegel‑Einzüge und relative Positionierung vertauschen

### TRANSPARENT_METAFILES {#TRANSPARENT-METAFILES}
```
public static int TRANSPARENT_METAFILES
```


Transparente Metadateien

### TRUNCATE_FONT_HEIGHT_LIKE_WP_6 {#TRUNCATE-FONT-HEIGHT-LIKE-WP-6}
```
public static int TRUNCATE_FONT_HEIGHT_LIKE_WP_6
```


Schrifthöhe wie WordPerfect 6 kürzen

### UI_COMPAT_97_TO_2003 {#UI-COMPAT-97-TO-2003}
```
public static int UI_COMPAT_97_TO_2003
```


### UL_TRAIL_SPACE {#UL-TRAIL-SPACE}
```
public static int UL_TRAIL_SPACE
```


Nachgestelltes Leerzeichen unterstreichen

### UNDERLINE_TAB_IN_NUM_LIST {#UNDERLINE-TAB-IN-NUM-LIST}
```
public static int UNDERLINE_TAB_IN_NUM_LIST
```


Tabulator in nummerierter Liste unterstreichen

### USE_ALT_KINSOKU_LINE_BREAK_RULES {#USE-ALT-KINSOKU-LINE-BREAK-RULES}
```
public static int USE_ALT_KINSOKU_LINE_BREAK_RULES
```


Alt‑Kinsoku‑Zeilenumbruchregeln verwenden

### USE_ANSI_KERNING_PAIRS {#USE-ANSI-KERNING-PAIRS}
```
public static int USE_ANSI_KERNING_PAIRS
```


ANSI‑Kerning‑Paare verwenden

### USE_FE_LAYOUT {#USE-FE-LAYOUT}
```
public static int USE_FE_LAYOUT
```


### USE_NORMAL_STYLE_FOR_LIST {#USE-NORMAL-STYLE-FOR-LIST}
```
public static int USE_NORMAL_STYLE_FOR_LIST
```


Normal‑Format für Liste verwenden

### USE_PRINTER_METRICS {#USE-PRINTER-METRICS}
```
public static int USE_PRINTER_METRICS
```


Drucker‑Metriken verwenden

### USE_SINGLE_BORDERFOR_CONTIGUOUS_CELLS {#USE-SINGLE-BORDERFOR-CONTIGUOUS-CELLS}
```
public static int USE_SINGLE_BORDERFOR_CONTIGUOUS_CELLS
```


Einzelnen Rand für zusammenhängende Zellen verwenden

### USE_WORD_2002_TABLE_STYLE_RULES {#USE-WORD-2002-TABLE-STYLE-RULES}
```
public static int USE_WORD_2002_TABLE_STYLE_RULES
```


Word‑2002‑Tabellenformatregeln verwenden

### USE_WORD_2010_TABLE_STYLE_RULES {#USE-WORD-2010-TABLE-STYLE-RULES}
```
public static int USE_WORD_2010_TABLE_STYLE_RULES
```


Word‑2010‑Tabellenformatregeln verwenden

### USE_WORD_97_LINE_BREAK_RULES {#USE-WORD-97-LINE-BREAK-RULES}
```
public static int USE_WORD_97_LINE_BREAK_RULES
```


Word‑97‑Zeilenumbruchregeln verwenden

### WP_JUSTIFICATION {#WP-JUSTIFICATION}
```
public static int WP_JUSTIFICATION
```


### WP_SPACE_WIDTH {#WP-SPACE-WIDTH}
```
public static int WP_SPACE_WIDTH
```


### WRAP_TRAIL_SPACES {#WRAP-TRAIL-SPACES}
```
public static int WRAP_TRAIL_SPACES
```


Nachgestellte Leerzeichen umbrechen

### length {#length}
```
public static int length
```


### fromName(String compatibilityName) {#fromName-java.lang.String}
```
public static int fromName(String compatibilityName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| compatibilityName | java.lang.String |  |

**Returns:**
int
### getName(int compatibility) {#getName-int}
```
public static String getName(int compatibility)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| compatibility | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int compatibility) {#toString-int}
```
public static String toString(int compatibility)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| compatibility | int |  |

**Returns:**
java.lang.String
