---
title: "MsWordVersion"
linktitle: "MsWordVersion"
second_title: "Aspose.Words para Java"
description: "Permite que Aspose.Wods imite el comportamiento de la aplicación específico de la versión de MS Word en Java."
type: docs
weight: 471
url: /es/java/com.aspose.words/mswordversion/
---

**Inheritance:**
java.lang.Object
```
public class MsWordVersion
```

Permite que Aspose.Wods imite el comportamiento de la aplicación específico de cada versión de MS Word.

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
| [WORD_2000](#WORD-2000) | Optimiza el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2000. |
| [WORD_2002](#WORD-2002) | Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2002 de MS Word. |
| [WORD_2003](#WORD-2003) | Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2003 de MS Word. |
| [WORD_2007](#WORD-2007) | Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2007 de MS Word. |
| [WORD_2010](#WORD-2010) | Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2010 de MS Word. |
| [WORD_2013](#WORD-2013) | Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2013 de MS Word. |
| [WORD_2016](#WORD-2016) | Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2016 de MS Word. |
| [WORD_2019](#WORD-2019) | Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2019 de MS Word. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String msWordVersionName)](#fromName-java.lang.String) |  |
| [getName(int msWordVersion)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int msWordVersion)](#toString-int) |  |
### WORD_2000 {#WORD-2000}
```
public static int WORD_2000
```


Optimiza el comportamiento de Aspose.Words para que coincida con la versión de MS Word 2000.

### WORD_2002 {#WORD-2002}
```
public static int WORD_2002
```


Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2002 de MS Word.

### WORD_2003 {#WORD-2003}
```
public static int WORD_2003
```


Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2003 de MS Word.

### WORD_2007 {#WORD-2007}
```
public static int WORD_2007
```


Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2007 de MS Word.

### WORD_2010 {#WORD-2010}
```
public static int WORD_2010
```


Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2010 de MS Word.

### WORD_2013 {#WORD-2013}
```
public static int WORD_2013
```


Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2013 de MS Word.

### WORD_2016 {#WORD-2016}
```
public static int WORD_2016
```


Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2016 de MS Word.

### WORD_2019 {#WORD-2019}
```
public static int WORD_2019
```


Optimizar el comportamiento de Aspose.Words para que coincida con la versión 2019 de MS Word.

### length {#length}
```
public static int length
```


### fromName(String msWordVersionName) {#fromName-java.lang.String}
```
public static int fromName(String msWordVersionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| msWordVersionName | java.lang.String |  |

**Returns:**
int
### getName(int msWordVersion) {#getName-int}
```
public static String getName(int msWordVersion)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| msWordVersion | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int msWordVersion) {#toString-int}
```
public static String toString(int msWordVersion)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| msWordVersion | int |  |

**Returns:**
java.lang.String
