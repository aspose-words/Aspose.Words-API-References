---
title: "Compatibility"
linktitle: "Compatibility"
second_title: "Aspose.Words para Java"
description: "Especifica los nombres de las opciones de compatibilidad en Java."
type: docs
weight: 119
url: /es/java/com.aspose.words/compatibility/
---

**Inheritance:**
java.lang.Object
```
public class Compatibility
```

Especifica los nombres de las opciones de compatibilidad.

 **Examples:** 

Mostrar cómo optimizar el documento para diferentes versiones de Microsoft Word.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ADJUST_LINE_HEIGHT_IN_TABLE](#ADJUST-LINE-HEIGHT-IN-TABLE) | Ajustar la altura de línea en la tabla |
| [ALIGN_TABLE_ROW_BY_ROW](#ALIGN-TABLE-ROW-BY-ROW) | Alinear filas de tabla por regla |
| [ALLOW_SPACE_OF_SAME_STYLE_IN_TABLE](#ALLOW-SPACE-OF-SAME-STYLE-IN-TABLE) | Permitir espacio del mismo estilo en la tabla |
| [APPLY_BREAKING_RULES](#APPLY-BREAKING-RULES) | Aplicar reglas de separación |
| [AUTOFIT_TO_FIRST_FIXED_WIDTH_CELL](#AUTOFIT-TO-FIRST-FIXED-WIDTH-CELL) | Ajuste automático a la primera celda de ancho fijo |
| [AUTO_SPACE_LIKE_WORD_95](#AUTO-SPACE-LIKE-WORD-95) | Espaciado automático como Word 95 |
| [BALANCE_SINGLE_BYTE_DOUBLE_BYTE_WIDTH](#BALANCE-SINGLE-BYTE-DOUBLE-BYTE-WIDTH) | Equilibrar anchos de un solo byte y de doble byte |
| [CACHED_COL_BALANCE](#CACHED-COL-BALANCE) | Equilibrado de columnas en caché |
| [CONV_MAIL_MERGE_ESC](#CONV-MAIL-MERGE-ESC) | Convertir escapes de combinación de correspondencia |
| [DISABLE_OPEN_TYPE_FONT_FORMATTING_FEATURES](#DISABLE-OPEN-TYPE-FONT-FORMATTING-FEATURES) | Desactivar características de formato de fuente OpenType |
| [DISPLAY_HANGUL_FIXED_WIDTH](#DISPLAY-HANGUL-FIXED-WIDTH) | Mostrar ancho fijo de Hangul |
| [DO_NOT_AUTOFIT_CONSTRAINED_TABLES](#DO-NOT-AUTOFIT-CONSTRAINED-TABLES) | No ajustar automáticamente tablas restringidas |
| [DO_NOT_BREAK_CONSTRAINED_FORCED_TABLE](#DO-NOT-BREAK-CONSTRAINED-FORCED-TABLE) | No dividir tablas forzadas restringidas |
| [DO_NOT_BREAK_WRAPPED_TABLES](#DO-NOT-BREAK-WRAPPED-TABLES) | No dividir tablas ajustadas |
| [DO_NOT_EXPAND_ON_SHIFT_RETURN](#DO-NOT-EXPAND-ON-SHIFT-RETURN) | No expandir con Mayús+Enter |
| [DO_NOT_LEAVE_BACKSLASH_ALONE](#DO-NOT-LEAVE-BACKSLASH-ALONE) | No dejar la barra invertida sola |
| [DO_NOT_SNAP_TO_GRID_IN_CELL](#DO-NOT-SNAP-TO-GRID-IN-CELL) | No ajustar a la cuadrícula en celdas |
| [DO_NOT_SUPPRESS_INDENTATION](#DO-NOT-SUPPRESS-INDENTATION) | No suprimir sangría |
| [DO_NOT_SUPPRESS_PARAGRAPH_BORDER](#DO-NOT-SUPPRESS-PARAGRAPH-BORDER) | No suprimir borde de párrafo |
| [DO_NOT_USE_EAST_ASIAN_BREAK_RULES](#DO-NOT-USE-EAST-ASIAN-BREAK-RULES) | No usar reglas de separación de Asia Oriental |
| [DO_NOT_USE_HTML_PARAGRAPH_AUTO_SPACING](#DO-NOT-USE-HTML-PARAGRAPH-AUTO-SPACING) | No usar espaciado automático de párrafos HTML |
| [DO_NOT_USE_INDENT_AS_NUMBERING_TAB_STOP](#DO-NOT-USE-INDENT-AS-NUMBERING-TAB-STOP) | No usar sangría como tabulación de numeración |
| [DO_NOT_VERT_ALIGN_CELL_WITH_SP](#DO-NOT-VERT-ALIGN-CELL-WITH-SP) | No alinear verticalmente la celda con espaciado |
| [DO_NOT_VERT_ALIGN_IN_TXBX](#DO-NOT-VERT-ALIGN-IN-TXBX) | No alinear verticalmente en cuadros de texto |
| [DO_NOT_WRAP_TEXT_WITH_PUNCT](#DO-NOT-WRAP-TEXT-WITH-PUNCT) | No ajustar texto con puntuación |
| [FOOTNOTE_LAYOUT_LIKE_WW_8](#FOOTNOTE-LAYOUT-LIKE-WW-8) | Diseño de nota al pie como Word 2000 |
| [FORGET_LAST_TAB_ALIGNMENT](#FORGET-LAST-TAB-ALIGNMENT) | Olvidar la alineación de la última tabulación |
| [GROW_AUTOFIT](#GROW-AUTOFIT) | Aumentar AutoFit |
| [LAYOUT_RAW_TABLE_WIDTH](#LAYOUT-RAW-TABLE-WIDTH) | Diseñar ancho bruto de tabla |
| [LAYOUT_TABLE_ROWS_APART](#LAYOUT-TABLE-ROWS-APART) | Diseñar filas de tabla separadas |
| [LINE_WRAP_LIKE_WORD_6](#LINE-WRAP-LIKE-WORD-6) | Ajuste de línea como Word 6 |
| [MW_SMALL_CAPS](#MW-SMALL-CAPS) |  |
| [NO_COLUMN_BALANCE](#NO-COLUMN-BALANCE) | Sin equilibrado de columnas |
| [NO_EXTRA_LINE_SPACING](#NO-EXTRA-LINE-SPACING) | Sin espaciado extra de línea |
| [NO_LEADING](#NO-LEADING) | Sin interlineado |
| [NO_SPACE_RAISE_LOWER](#NO-SPACE-RAISE-LOWER) | Sin espacio subir o bajar |
| [NO_TAB_HANG_IND](#NO-TAB-HANG-IND) | Sin sangría colgante de tabulación |
| [OVERRIDE_TABLE_STYLE_FONT_SIZE_AND_JUSTIFICATION](#OVERRIDE-TABLE-STYLE-FONT-SIZE-AND-JUSTIFICATION) | Sobrescribir tamaño de fuente y justificación del estilo de tabla |
| [PRINT_BODY_TEXT_BEFORE_HEADER](#PRINT-BODY-TEXT-BEFORE-HEADER) | Imprimir texto del cuerpo antes del encabezado |
| [PRINT_COL_BLACK](#PRINT-COL-BLACK) | Imprimir fondo de columna |
| [SELECT_FLD_WITH_FIRST_OR_LAST_CHAR](#SELECT-FLD-WITH-FIRST-OR-LAST-CHAR) | Seleccionar campo con el primer o último carácter |
| [SHAPE_LAYOUT_LIKE_WW_8](#SHAPE-LAYOUT-LIKE-WW-8) | Diseño de forma como Word 2000 |
| [SHOW_BREAKS_IN_FRAMES](#SHOW-BREAKS-IN-FRAMES) | Mostrar saltos en marcos |
| [SPACE_FOR_UL](#SPACE-FOR-UL) | Espacio para subrayado |
| [SPACING_IN_WHOLE_POINTS](#SPACING-IN-WHOLE-POINTS) | Espaciado en puntos completos |
| [SPLIT_PG_BREAK_AND_PARA_MARK](#SPLIT-PG-BREAK-AND-PARA-MARK) | Dividir salto de página y marca de párrafo |
| [SUB_FONT_BY_SIZE](#SUB-FONT-BY-SIZE) | Sustituir fuente por tamaño |
| [SUPPRESS_BOTTOM_SPACING](#SUPPRESS-BOTTOM-SPACING) | Suprimir espaciado inferior |
| [SUPPRESS_SP_BF_AFTER_PG_BRK](#SUPPRESS-SP-BF-AFTER-PG-BRK) | Suprimir espacio antes del salto de párrafo |
| [SUPPRESS_TOP_LINE_SPACING_WP](#SUPPRESS-TOP-LINE-SPACING-WP) | Suprimir espaciado superior de línea en WordPerfect |
| [SUPPRESS_TOP_SPACING](#SUPPRESS-TOP-SPACING) | Suprimir espaciado superior |
| [SUPPRESS_TOP_SPACING_AT_TOP_OF_PAGE](#SUPPRESS-TOP-SPACING-AT-TOP-OF-PAGE) | Suprimir espaciado superior de línea en WordPerfect |
| [SWAP_BORDERS_ODD_FACING_PGS](#SWAP-BORDERS-ODD-FACING-PGS) | Intercambiar bordes en páginas impares |
| [SWAP_INSIDE_AND_OUTSIDE_FOR_MIRROR_INDENTS_AND_RELATIVE_POSITIONING](#SWAP-INSIDE-AND-OUTSIDE-FOR-MIRROR-INDENTS-AND-RELATIVE-POSITIONING) | Intercambiar interior y exterior para sangrías espejo y posicionamiento relativo |
| [TRANSPARENT_METAFILES](#TRANSPARENT-METAFILES) | Metaficheros transparentes |
| [TRUNCATE_FONT_HEIGHT_LIKE_WP_6](#TRUNCATE-FONT-HEIGHT-LIKE-WP-6) | Truncar la altura de la fuente como WordPerfect 6 |
| [UI_COMPAT_97_TO_2003](#UI-COMPAT-97-TO-2003) |  |
| [UL_TRAIL_SPACE](#UL-TRAIL-SPACE) | Subrayar el espacio final |
| [UNDERLINE_TAB_IN_NUM_LIST](#UNDERLINE-TAB-IN-NUM-LIST) | Subrayar la tabulación en una lista numerada |
| [USE_ALT_KINSOKU_LINE_BREAK_RULES](#USE-ALT-KINSOKU-LINE-BREAK-RULES) | Usar reglas de salto de línea Alt Kinsoku |
| [USE_ANSI_KERNING_PAIRS](#USE-ANSI-KERNING-PAIRS) | Usar pares de interletraje ANSI |
| [USE_FE_LAYOUT](#USE-FE-LAYOUT) |  |
| [USE_NORMAL_STYLE_FOR_LIST](#USE-NORMAL-STYLE-FOR-LIST) | Usar estilo normal para la lista |
| [USE_PRINTER_METRICS](#USE-PRINTER-METRICS) | Usar métricas de la impresora |
| [USE_SINGLE_BORDERFOR_CONTIGUOUS_CELLS](#USE-SINGLE-BORDERFOR-CONTIGUOUS-CELLS) | Usar borde único para celdas contiguas |
| [USE_WORD_2002_TABLE_STYLE_RULES](#USE-WORD-2002-TABLE-STYLE-RULES) | Usar reglas de estilo de tabla de Word 2002 |
| [USE_WORD_2010_TABLE_STYLE_RULES](#USE-WORD-2010-TABLE-STYLE-RULES) | Usar reglas de estilo de tabla de Word 2010 |
| [USE_WORD_97_LINE_BREAK_RULES](#USE-WORD-97-LINE-BREAK-RULES) | Usar reglas de salto de línea de Word 97 |
| [WP_JUSTIFICATION](#WP-JUSTIFICATION) |  |
| [WP_SPACE_WIDTH](#WP-SPACE-WIDTH) |  |
| [WRAP_TRAIL_SPACES](#WRAP-TRAIL-SPACES) | Envolver espacios finales |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String compatibilityName)](#fromName-java.lang.String) |  |
| [getName(int compatibility)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int compatibility)](#toString-int) |  |
### ADJUST_LINE_HEIGHT_IN_TABLE {#ADJUST-LINE-HEIGHT-IN-TABLE}
```
public static int ADJUST_LINE_HEIGHT_IN_TABLE
```


Ajustar la altura de línea en la tabla

### ALIGN_TABLE_ROW_BY_ROW {#ALIGN-TABLE-ROW-BY-ROW}
```
public static int ALIGN_TABLE_ROW_BY_ROW
```


Alinear filas de tabla por regla

### ALLOW_SPACE_OF_SAME_STYLE_IN_TABLE {#ALLOW-SPACE-OF-SAME-STYLE-IN-TABLE}
```
public static int ALLOW_SPACE_OF_SAME_STYLE_IN_TABLE
```


Permitir espacio del mismo estilo en la tabla

### APPLY_BREAKING_RULES {#APPLY-BREAKING-RULES}
```
public static int APPLY_BREAKING_RULES
```


Aplicar reglas de separación

### AUTOFIT_TO_FIRST_FIXED_WIDTH_CELL {#AUTOFIT-TO-FIRST-FIXED-WIDTH-CELL}
```
public static int AUTOFIT_TO_FIRST_FIXED_WIDTH_CELL
```


Ajuste automático a la primera celda de ancho fijo

### AUTO_SPACE_LIKE_WORD_95 {#AUTO-SPACE-LIKE-WORD-95}
```
public static int AUTO_SPACE_LIKE_WORD_95
```


Espaciado automático como Word 95

### BALANCE_SINGLE_BYTE_DOUBLE_BYTE_WIDTH {#BALANCE-SINGLE-BYTE-DOUBLE-BYTE-WIDTH}
```
public static int BALANCE_SINGLE_BYTE_DOUBLE_BYTE_WIDTH
```


Equilibrar anchos de un solo byte y de doble byte

### CACHED_COL_BALANCE {#CACHED-COL-BALANCE}
```
public static int CACHED_COL_BALANCE
```


Equilibrado de columnas en caché

### CONV_MAIL_MERGE_ESC {#CONV-MAIL-MERGE-ESC}
```
public static int CONV_MAIL_MERGE_ESC
```


Convertir escapes de combinación de correspondencia

### DISABLE_OPEN_TYPE_FONT_FORMATTING_FEATURES {#DISABLE-OPEN-TYPE-FONT-FORMATTING-FEATURES}
```
public static int DISABLE_OPEN_TYPE_FONT_FORMATTING_FEATURES
```


Desactivar características de formato de fuente OpenType

### DISPLAY_HANGUL_FIXED_WIDTH {#DISPLAY-HANGUL-FIXED-WIDTH}
```
public static int DISPLAY_HANGUL_FIXED_WIDTH
```


Mostrar ancho fijo de Hangul

### DO_NOT_AUTOFIT_CONSTRAINED_TABLES {#DO-NOT-AUTOFIT-CONSTRAINED-TABLES}
```
public static int DO_NOT_AUTOFIT_CONSTRAINED_TABLES
```


No ajustar automáticamente tablas restringidas

### DO_NOT_BREAK_CONSTRAINED_FORCED_TABLE {#DO-NOT-BREAK-CONSTRAINED-FORCED-TABLE}
```
public static int DO_NOT_BREAK_CONSTRAINED_FORCED_TABLE
```


No dividir tablas forzadas restringidas

### DO_NOT_BREAK_WRAPPED_TABLES {#DO-NOT-BREAK-WRAPPED-TABLES}
```
public static int DO_NOT_BREAK_WRAPPED_TABLES
```


No dividir tablas ajustadas

### DO_NOT_EXPAND_ON_SHIFT_RETURN {#DO-NOT-EXPAND-ON-SHIFT-RETURN}
```
public static int DO_NOT_EXPAND_ON_SHIFT_RETURN
```


No expandir con Mayús+Enter

### DO_NOT_LEAVE_BACKSLASH_ALONE {#DO-NOT-LEAVE-BACKSLASH-ALONE}
```
public static int DO_NOT_LEAVE_BACKSLASH_ALONE
```


No dejar la barra invertida sola

### DO_NOT_SNAP_TO_GRID_IN_CELL {#DO-NOT-SNAP-TO-GRID-IN-CELL}
```
public static int DO_NOT_SNAP_TO_GRID_IN_CELL
```


No ajustar a la cuadrícula en celdas

### DO_NOT_SUPPRESS_INDENTATION {#DO-NOT-SUPPRESS-INDENTATION}
```
public static int DO_NOT_SUPPRESS_INDENTATION
```


No suprimir sangría

### DO_NOT_SUPPRESS_PARAGRAPH_BORDER {#DO-NOT-SUPPRESS-PARAGRAPH-BORDER}
```
public static int DO_NOT_SUPPRESS_PARAGRAPH_BORDER
```


No suprimir borde de párrafo

### DO_NOT_USE_EAST_ASIAN_BREAK_RULES {#DO-NOT-USE-EAST-ASIAN-BREAK-RULES}
```
public static int DO_NOT_USE_EAST_ASIAN_BREAK_RULES
```


No usar reglas de separación de Asia Oriental

### DO_NOT_USE_HTML_PARAGRAPH_AUTO_SPACING {#DO-NOT-USE-HTML-PARAGRAPH-AUTO-SPACING}
```
public static int DO_NOT_USE_HTML_PARAGRAPH_AUTO_SPACING
```


No usar espaciado automático de párrafos HTML

### DO_NOT_USE_INDENT_AS_NUMBERING_TAB_STOP {#DO-NOT-USE-INDENT-AS-NUMBERING-TAB-STOP}
```
public static int DO_NOT_USE_INDENT_AS_NUMBERING_TAB_STOP
```


No usar sangría como tabulación de numeración

### DO_NOT_VERT_ALIGN_CELL_WITH_SP {#DO-NOT-VERT-ALIGN-CELL-WITH-SP}
```
public static int DO_NOT_VERT_ALIGN_CELL_WITH_SP
```


No alinear verticalmente la celda con espaciado

### DO_NOT_VERT_ALIGN_IN_TXBX {#DO-NOT-VERT-ALIGN-IN-TXBX}
```
public static int DO_NOT_VERT_ALIGN_IN_TXBX
```


No alinear verticalmente en cuadros de texto

### DO_NOT_WRAP_TEXT_WITH_PUNCT {#DO-NOT-WRAP-TEXT-WITH-PUNCT}
```
public static int DO_NOT_WRAP_TEXT_WITH_PUNCT
```


No ajustar texto con puntuación

### FOOTNOTE_LAYOUT_LIKE_WW_8 {#FOOTNOTE-LAYOUT-LIKE-WW-8}
```
public static int FOOTNOTE_LAYOUT_LIKE_WW_8
```


Diseño de nota al pie como Word 2000

### FORGET_LAST_TAB_ALIGNMENT {#FORGET-LAST-TAB-ALIGNMENT}
```
public static int FORGET_LAST_TAB_ALIGNMENT
```


Olvidar la alineación de la última tabulación

### GROW_AUTOFIT {#GROW-AUTOFIT}
```
public static int GROW_AUTOFIT
```


Aumentar AutoFit

### LAYOUT_RAW_TABLE_WIDTH {#LAYOUT-RAW-TABLE-WIDTH}
```
public static int LAYOUT_RAW_TABLE_WIDTH
```


Diseñar ancho bruto de tabla

### LAYOUT_TABLE_ROWS_APART {#LAYOUT-TABLE-ROWS-APART}
```
public static int LAYOUT_TABLE_ROWS_APART
```


Diseñar filas de tabla separadas

### LINE_WRAP_LIKE_WORD_6 {#LINE-WRAP-LIKE-WORD-6}
```
public static int LINE_WRAP_LIKE_WORD_6
```


Ajuste de línea como Word 6

### MW_SMALL_CAPS {#MW-SMALL-CAPS}
```
public static int MW_SMALL_CAPS
```


### NO_COLUMN_BALANCE {#NO-COLUMN-BALANCE}
```
public static int NO_COLUMN_BALANCE
```


Sin equilibrado de columnas

### NO_EXTRA_LINE_SPACING {#NO-EXTRA-LINE-SPACING}
```
public static int NO_EXTRA_LINE_SPACING
```


Sin espaciado extra de línea

### NO_LEADING {#NO-LEADING}
```
public static int NO_LEADING
```


Sin interlineado

### NO_SPACE_RAISE_LOWER {#NO-SPACE-RAISE-LOWER}
```
public static int NO_SPACE_RAISE_LOWER
```


Sin espacio subir o bajar

### NO_TAB_HANG_IND {#NO-TAB-HANG-IND}
```
public static int NO_TAB_HANG_IND
```


Sin sangría colgante de tabulación

### OVERRIDE_TABLE_STYLE_FONT_SIZE_AND_JUSTIFICATION {#OVERRIDE-TABLE-STYLE-FONT-SIZE-AND-JUSTIFICATION}
```
public static int OVERRIDE_TABLE_STYLE_FONT_SIZE_AND_JUSTIFICATION
```


Sobrescribir tamaño de fuente y justificación del estilo de tabla

### PRINT_BODY_TEXT_BEFORE_HEADER {#PRINT-BODY-TEXT-BEFORE-HEADER}
```
public static int PRINT_BODY_TEXT_BEFORE_HEADER
```


Imprimir texto del cuerpo antes del encabezado

### PRINT_COL_BLACK {#PRINT-COL-BLACK}
```
public static int PRINT_COL_BLACK
```


Imprimir fondo de columna

### SELECT_FLD_WITH_FIRST_OR_LAST_CHAR {#SELECT-FLD-WITH-FIRST-OR-LAST-CHAR}
```
public static int SELECT_FLD_WITH_FIRST_OR_LAST_CHAR
```


Seleccionar campo con el primer o último carácter

### SHAPE_LAYOUT_LIKE_WW_8 {#SHAPE-LAYOUT-LIKE-WW-8}
```
public static int SHAPE_LAYOUT_LIKE_WW_8
```


Diseño de forma como Word 2000

### SHOW_BREAKS_IN_FRAMES {#SHOW-BREAKS-IN-FRAMES}
```
public static int SHOW_BREAKS_IN_FRAMES
```


Mostrar saltos en marcos

### SPACE_FOR_UL {#SPACE-FOR-UL}
```
public static int SPACE_FOR_UL
```


Espacio para subrayado

### SPACING_IN_WHOLE_POINTS {#SPACING-IN-WHOLE-POINTS}
```
public static int SPACING_IN_WHOLE_POINTS
```


Espaciado en puntos completos

### SPLIT_PG_BREAK_AND_PARA_MARK {#SPLIT-PG-BREAK-AND-PARA-MARK}
```
public static int SPLIT_PG_BREAK_AND_PARA_MARK
```


Dividir salto de página y marca de párrafo

### SUB_FONT_BY_SIZE {#SUB-FONT-BY-SIZE}
```
public static int SUB_FONT_BY_SIZE
```


Sustituir fuente por tamaño

### SUPPRESS_BOTTOM_SPACING {#SUPPRESS-BOTTOM-SPACING}
```
public static int SUPPRESS_BOTTOM_SPACING
```


Suprimir espaciado inferior

### SUPPRESS_SP_BF_AFTER_PG_BRK {#SUPPRESS-SP-BF-AFTER-PG-BRK}
```
public static int SUPPRESS_SP_BF_AFTER_PG_BRK
```


Suprimir espacio antes del salto de párrafo

### SUPPRESS_TOP_LINE_SPACING_WP {#SUPPRESS-TOP-LINE-SPACING-WP}
```
public static int SUPPRESS_TOP_LINE_SPACING_WP
```


Suprimir espaciado superior de línea en WordPerfect

### SUPPRESS_TOP_SPACING {#SUPPRESS-TOP-SPACING}
```
public static int SUPPRESS_TOP_SPACING
```


Suprimir espaciado superior

### SUPPRESS_TOP_SPACING_AT_TOP_OF_PAGE {#SUPPRESS-TOP-SPACING-AT-TOP-OF-PAGE}
```
public static int SUPPRESS_TOP_SPACING_AT_TOP_OF_PAGE
```


Suprimir espaciado superior de línea en WordPerfect

### SWAP_BORDERS_ODD_FACING_PGS {#SWAP-BORDERS-ODD-FACING-PGS}
```
public static int SWAP_BORDERS_ODD_FACING_PGS
```


Intercambiar bordes en páginas impares

### SWAP_INSIDE_AND_OUTSIDE_FOR_MIRROR_INDENTS_AND_RELATIVE_POSITIONING {#SWAP-INSIDE-AND-OUTSIDE-FOR-MIRROR-INDENTS-AND-RELATIVE-POSITIONING}
```
public static int SWAP_INSIDE_AND_OUTSIDE_FOR_MIRROR_INDENTS_AND_RELATIVE_POSITIONING
```


Intercambiar interior y exterior para sangrías espejo y posicionamiento relativo

### TRANSPARENT_METAFILES {#TRANSPARENT-METAFILES}
```
public static int TRANSPARENT_METAFILES
```


Metaficheros transparentes

### TRUNCATE_FONT_HEIGHT_LIKE_WP_6 {#TRUNCATE-FONT-HEIGHT-LIKE-WP-6}
```
public static int TRUNCATE_FONT_HEIGHT_LIKE_WP_6
```


Truncar la altura de la fuente como WordPerfect 6

### UI_COMPAT_97_TO_2003 {#UI-COMPAT-97-TO-2003}
```
public static int UI_COMPAT_97_TO_2003
```


### UL_TRAIL_SPACE {#UL-TRAIL-SPACE}
```
public static int UL_TRAIL_SPACE
```


Subrayar el espacio final

### UNDERLINE_TAB_IN_NUM_LIST {#UNDERLINE-TAB-IN-NUM-LIST}
```
public static int UNDERLINE_TAB_IN_NUM_LIST
```


Subrayar la tabulación en una lista numerada

### USE_ALT_KINSOKU_LINE_BREAK_RULES {#USE-ALT-KINSOKU-LINE-BREAK-RULES}
```
public static int USE_ALT_KINSOKU_LINE_BREAK_RULES
```


Usar reglas de salto de línea Alt Kinsoku

### USE_ANSI_KERNING_PAIRS {#USE-ANSI-KERNING-PAIRS}
```
public static int USE_ANSI_KERNING_PAIRS
```


Usar pares de interletraje ANSI

### USE_FE_LAYOUT {#USE-FE-LAYOUT}
```
public static int USE_FE_LAYOUT
```


### USE_NORMAL_STYLE_FOR_LIST {#USE-NORMAL-STYLE-FOR-LIST}
```
public static int USE_NORMAL_STYLE_FOR_LIST
```


Usar estilo normal para la lista

### USE_PRINTER_METRICS {#USE-PRINTER-METRICS}
```
public static int USE_PRINTER_METRICS
```


Usar métricas de la impresora

### USE_SINGLE_BORDERFOR_CONTIGUOUS_CELLS {#USE-SINGLE-BORDERFOR-CONTIGUOUS-CELLS}
```
public static int USE_SINGLE_BORDERFOR_CONTIGUOUS_CELLS
```


Usar borde único para celdas contiguas

### USE_WORD_2002_TABLE_STYLE_RULES {#USE-WORD-2002-TABLE-STYLE-RULES}
```
public static int USE_WORD_2002_TABLE_STYLE_RULES
```


Usar reglas de estilo de tabla de Word 2002

### USE_WORD_2010_TABLE_STYLE_RULES {#USE-WORD-2010-TABLE-STYLE-RULES}
```
public static int USE_WORD_2010_TABLE_STYLE_RULES
```


Usar reglas de estilo de tabla de Word 2010

### USE_WORD_97_LINE_BREAK_RULES {#USE-WORD-97-LINE-BREAK-RULES}
```
public static int USE_WORD_97_LINE_BREAK_RULES
```


Usar reglas de salto de línea de Word 97

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


Envolver espacios finales

### length {#length}
```
public static int length
```


### fromName(String compatibilityName) {#fromName-java.lang.String}
```
public static int fromName(String compatibilityName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| compatibilityName | java.lang.String |  |

**Returns:**
int
### getName(int compatibility) {#getName-int}
```
public static String getName(int compatibility)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| compatibilidad | int |  |

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| compatibilidad | int |  |

**Returns:**
java.lang.String
