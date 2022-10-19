---
title: CompatibilityOptions
second_title: Aspose.Words for Java API Reference
description: Contains compatibility options that is the user preferences entered on the Compatibility tab of the Options dialog in Microsoft Word.
type: docs
weight: 86
url: /java/com.aspose.words/compatibilityoptions/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class CompatibilityOptions implements Cloneable
```

Contains compatibility options (that is, the user preferences entered on the **Compatibility** tab of the **Options** dialog in Microsoft Word).

To learn more, visit the **Detect File Format and Check Format Compatibility** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [optimizeFor(int version)](#optimizeFor-int-) |  |
| [getNoTabHangInd()](#getNoTabHangInd--) | Do Not Create Custom Tab Stop for Hanging Indent. |
| [setNoTabHangInd(boolean value)](#setNoTabHangInd-boolean-) | Do Not Create Custom Tab Stop for Hanging Indent. |
| [getNoSpaceRaiseLower()](#getNoSpaceRaiseLower--) | Do Not Increase Line Height for Raised/Lowered Text. |
| [setNoSpaceRaiseLower(boolean value)](#setNoSpaceRaiseLower-boolean-) | Do Not Increase Line Height for Raised/Lowered Text. |
| [getSuppressSpBfAfterPgBrk()](#getSuppressSpBfAfterPgBrk--) | Do Not Use Space Before On First Line After a Page Break. |
| [setSuppressSpBfAfterPgBrk(boolean value)](#setSuppressSpBfAfterPgBrk-boolean-) | Do Not Use Space Before On First Line After a Page Break. |
| [getWrapTrailSpaces()](#getWrapTrailSpaces--) | Line Wrap Trailing Spaces. |
| [setWrapTrailSpaces(boolean value)](#setWrapTrailSpaces-boolean-) | Line Wrap Trailing Spaces. |
| [getPrintColBlack()](#getPrintColBlack--) | Print Colors as Black And White without Dithering. |
| [setPrintColBlack(boolean value)](#setPrintColBlack-boolean-) | Print Colors as Black And White without Dithering. |
| [getNoColumnBalance()](#getNoColumnBalance--) | Do Not Balance Text Columns within a Section. |
| [setNoColumnBalance(boolean value)](#setNoColumnBalance-boolean-) | Do Not Balance Text Columns within a Section. |
| [getConvMailMergeEsc()](#getConvMailMergeEsc--) | Treat Backslash Quotation Delimiter as Two Quotation Marks. |
| [setConvMailMergeEsc(boolean value)](#setConvMailMergeEsc-boolean-) | Treat Backslash Quotation Delimiter as Two Quotation Marks. |
| [getSuppressTopSpacing()](#getSuppressTopSpacing--) | Ignore Minimum and Exact Line Height for First Line on Page. |
| [setSuppressTopSpacing(boolean value)](#setSuppressTopSpacing-boolean-) | Ignore Minimum and Exact Line Height for First Line on Page. |
| [getUseSingleBorderforContiguousCells()](#getUseSingleBorderforContiguousCells--) | Use Simplified Rules For Table Border Conflicts. |
| [setUseSingleBorderforContiguousCells(boolean value)](#setUseSingleBorderforContiguousCells-boolean-) | Use Simplified Rules For Table Border Conflicts. |
| [getTransparentMetafiles()](#getTransparentMetafiles--) | Specifies not to blank the area behind metafile pictures. |
| [setTransparentMetafiles(boolean value)](#setTransparentMetafiles-boolean-) | Specifies not to blank the area behind metafile pictures. |
| [getShowBreaksInFrames()](#getShowBreaksInFrames--) | Display Page/Column Breaks Present in Frames. |
| [setShowBreaksInFrames(boolean value)](#setShowBreaksInFrames-boolean-) | Display Page/Column Breaks Present in Frames. |
| [getSwapBordersFacingPgs()](#getSwapBordersFacingPgs--) | Swap Paragraph Borders on Odd Numbered Pages. |
| [setSwapBordersFacingPgs(boolean value)](#setSwapBordersFacingPgs-boolean-) | Swap Paragraph Borders on Odd Numbered Pages. |
| [getDoNotLeaveBackslashAlone()](#getDoNotLeaveBackslashAlone--) | Convert Backslash To Yen Sign When Entered. |
| [setDoNotLeaveBackslashAlone(boolean value)](#setDoNotLeaveBackslashAlone-boolean-) | Convert Backslash To Yen Sign When Entered. |
| [getDoNotExpandShiftReturn()](#getDoNotExpandShiftReturn--) | Don't Justify Lines Ending in Soft Line Break. |
| [setDoNotExpandShiftReturn(boolean value)](#setDoNotExpandShiftReturn-boolean-) | Don't Justify Lines Ending in Soft Line Break. |
| [getUlTrailSpace()](#getUlTrailSpace--) | Underline All Trailing Spaces. |
| [setUlTrailSpace(boolean value)](#setUlTrailSpace-boolean-) | Underline All Trailing Spaces. |
| [getBalanceSingleByteDoubleByteWidth()](#getBalanceSingleByteDoubleByteWidth--) | Balance Single Byte and Double Byte Characters. |
| [setBalanceSingleByteDoubleByteWidth(boolean value)](#setBalanceSingleByteDoubleByteWidth-boolean-) | Balance Single Byte and Double Byte Characters. |
| [getSuppressSpacingAtTopOfPage()](#getSuppressSpacingAtTopOfPage--) | Ignore Minimum Line Height for First Line on Page. |
| [setSuppressSpacingAtTopOfPage(boolean value)](#setSuppressSpacingAtTopOfPage-boolean-) | Ignore Minimum Line Height for First Line on Page. |
| [getSpacingInWholePoints()](#getSpacingInWholePoints--) | Only Expand/Condense Text By Whole Points. |
| [setSpacingInWholePoints(boolean value)](#setSpacingInWholePoints-boolean-) | Only Expand/Condense Text By Whole Points. |
| [getPrintBodyTextBeforeHeader()](#getPrintBodyTextBeforeHeader--) | Print Body Text before Header/Footer Contents. |
| [setPrintBodyTextBeforeHeader(boolean value)](#setPrintBodyTextBeforeHeader-boolean-) | Print Body Text before Header/Footer Contents. |
| [getNoLeading()](#getNoLeading--) | Do Not Add Leading Between Lines of Text. |
| [setNoLeading(boolean value)](#setNoLeading-boolean-) | Do Not Add Leading Between Lines of Text. |
| [getSpaceForUL()](#getSpaceForUL--) | Add Additional Space Below Baseline For Underlined East Asian Text. |
| [setSpaceForUL(boolean value)](#setSpaceForUL-boolean-) | Add Additional Space Below Baseline For Underlined East Asian Text. |
| [getMWSmallCaps()](#getMWSmallCaps--) | Emulate Word 5.x for the Macintosh Small Caps Formatting. |
| [setMWSmallCaps(boolean value)](#setMWSmallCaps-boolean-) | Emulate Word 5.x for the Macintosh Small Caps Formatting. |
| [getSuppressTopSpacingWP()](#getSuppressTopSpacingWP--) | Emulate WordPerfect 5.x Line Spacing. |
| [setSuppressTopSpacingWP(boolean value)](#setSuppressTopSpacingWP-boolean-) | Emulate WordPerfect 5.x Line Spacing. |
| [getTruncateFontHeightsLikeWP6()](#getTruncateFontHeightsLikeWP6--) | Emulate WordPerfect 6.x Font Height Calculation. |
| [setTruncateFontHeightsLikeWP6(boolean value)](#setTruncateFontHeightsLikeWP6-boolean-) | Emulate WordPerfect 6.x Font Height Calculation. |
| [getSubFontBySize()](#getSubFontBySize--) | Increase Priority Of Font Size During Font Substitution. |
| [setSubFontBySize(boolean value)](#setSubFontBySize-boolean-) | Increase Priority Of Font Size During Font Substitution. |
| [getLineWrapLikeWord6()](#getLineWrapLikeWord6--) | Emulate Word 6.0 Line Wrapping for East Asian Text. |
| [setLineWrapLikeWord6(boolean value)](#setLineWrapLikeWord6-boolean-) | Emulate Word 6.0 Line Wrapping for East Asian Text. |
| [getDoNotSuppressParagraphBorders()](#getDoNotSuppressParagraphBorders--) | Do Not Suppress Paragraph Borders Next To Frames. |
| [setDoNotSuppressParagraphBorders(boolean value)](#setDoNotSuppressParagraphBorders-boolean-) | Do Not Suppress Paragraph Borders Next To Frames. |
| [getNoExtraLineSpacing()](#getNoExtraLineSpacing--) | Do Not Center Content on Lines With Exact Line Height. |
| [setNoExtraLineSpacing(boolean value)](#setNoExtraLineSpacing-boolean-) | Do Not Center Content on Lines With Exact Line Height. |
| [getSuppressBottomSpacing()](#getSuppressBottomSpacing--) | Ignore Exact Line Height for Last Line on Page. |
| [setSuppressBottomSpacing(boolean value)](#setSuppressBottomSpacing-boolean-) | Ignore Exact Line Height for Last Line on Page. |
| [getWPSpaceWidth()](#getWPSpaceWidth--) | Specifies whether to set the width of a space as is done in WordPerfect 5.x. |
| [setWPSpaceWidth(boolean value)](#setWPSpaceWidth-boolean-) | Specifies whether to set the width of a space as is done in WordPerfect 5.x. |
| [getWPJustification()](#getWPJustification--) | Emulate WordPerfect 6.x Paragraph Justification. |
| [setWPJustification(boolean value)](#setWPJustification-boolean-) | Emulate WordPerfect 6.x Paragraph Justification. |
| [getUsePrinterMetrics()](#getUsePrinterMetrics--) | Use Printer Metrics To Display Documents. |
| [setUsePrinterMetrics(boolean value)](#setUsePrinterMetrics-boolean-) | Use Printer Metrics To Display Documents. |
| [getShapeLayoutLikeWW8()](#getShapeLayoutLikeWW8--) | Emulate Word 97 Text Wrapping Around Floating Objects. |
| [setShapeLayoutLikeWW8(boolean value)](#setShapeLayoutLikeWW8-boolean-) | Emulate Word 97 Text Wrapping Around Floating Objects. |
| [getFootnoteLayoutLikeWW8()](#getFootnoteLayoutLikeWW8--) | Emulate Word 6.x/95/97 Footnote Placement. |
| [setFootnoteLayoutLikeWW8(boolean value)](#setFootnoteLayoutLikeWW8-boolean-) | Emulate Word 6.x/95/97 Footnote Placement. |
| [getDoNotUseHTMLParagraphAutoSpacing()](#getDoNotUseHTMLParagraphAutoSpacing--) | Use Fixed Paragraph Spacing for HTML Auto Setting. |
| [setDoNotUseHTMLParagraphAutoSpacing(boolean value)](#setDoNotUseHTMLParagraphAutoSpacing-boolean-) | Use Fixed Paragraph Spacing for HTML Auto Setting. |
| [getAdjustLineHeightInTable()](#getAdjustLineHeightInTable--) | Add Document Grid Line Pitch To Lines in Table Cells. |
| [setAdjustLineHeightInTable(boolean value)](#setAdjustLineHeightInTable-boolean-) | Add Document Grid Line Pitch To Lines in Table Cells. |
| [getForgetLastTabAlignment()](#getForgetLastTabAlignment--) | Ignore Width of Last Tab Stop When Aligning Paragraph If It Is Not Left Aligned. |
| [setForgetLastTabAlignment(boolean value)](#setForgetLastTabAlignment-boolean-) | Ignore Width of Last Tab Stop When Aligning Paragraph If It Is Not Left Aligned. |
| [getAutoSpaceLikeWord95()](#getAutoSpaceLikeWord95--) | Emulate Word 95 Full-Width Character Spacing. |
| [setAutoSpaceLikeWord95(boolean value)](#setAutoSpaceLikeWord95-boolean-) | Emulate Word 95 Full-Width Character Spacing. |
| [getAlignTablesRowByRow()](#getAlignTablesRowByRow--) | Align Table Rows Independently. |
| [setAlignTablesRowByRow(boolean value)](#setAlignTablesRowByRow-boolean-) | Align Table Rows Independently. |
| [getLayoutRawTableWidth()](#getLayoutRawTableWidth--) | Ignore Space Before Table When Deciding If Table Should Wrap Floating Object. |
| [setLayoutRawTableWidth(boolean value)](#setLayoutRawTableWidth-boolean-) | Ignore Space Before Table When Deciding If Table Should Wrap Floating Object. |
| [getLayoutTableRowsApart()](#getLayoutTableRowsApart--) | Allow Table Rows to Wrap Inline Objects Independently. |
| [setLayoutTableRowsApart(boolean value)](#setLayoutTableRowsApart-boolean-) | Allow Table Rows to Wrap Inline Objects Independently. |
| [getUseWord97LineBreakRules()](#getUseWord97LineBreakRules--) | Emulate Word 97 East Asian Line Breaking. |
| [setUseWord97LineBreakRules(boolean value)](#setUseWord97LineBreakRules-boolean-) | Emulate Word 97 East Asian Line Breaking. |
| [getDoNotBreakWrappedTables()](#getDoNotBreakWrappedTables--) | Do Not Allow Floating Tables To Break Across Pages. |
| [setDoNotBreakWrappedTables(boolean value)](#setDoNotBreakWrappedTables-boolean-) | Do Not Allow Floating Tables To Break Across Pages. |
| [getDoNotSnapToGridInCell()](#getDoNotSnapToGridInCell--) | Do Not Snap to Document Grid in Table Cells with Objects. |
| [setDoNotSnapToGridInCell(boolean value)](#setDoNotSnapToGridInCell-boolean-) | Do Not Snap to Document Grid in Table Cells with Objects. |
| [getSelectFldWithFirstOrLastChar()](#getSelectFldWithFirstOrLastChar--) | Select Field When First or Last Character Is Selected. |
| [setSelectFldWithFirstOrLastChar(boolean value)](#setSelectFldWithFirstOrLastChar-boolean-) | Select Field When First or Last Character Is Selected. |
| [getApplyBreakingRules()](#getApplyBreakingRules--) | Use Legacy Ethiopic and Amharic Line Breaking Rules. |
| [setApplyBreakingRules(boolean value)](#setApplyBreakingRules-boolean-) | Use Legacy Ethiopic and Amharic Line Breaking Rules. |
| [getDoNotWrapTextWithPunct()](#getDoNotWrapTextWithPunct--) | Do Not Allow Hanging Punctuation With Character Grid. |
| [setDoNotWrapTextWithPunct(boolean value)](#setDoNotWrapTextWithPunct-boolean-) | Do Not Allow Hanging Punctuation With Character Grid. |
| [getDoNotUseEastAsianBreakRules()](#getDoNotUseEastAsianBreakRules--) | Do Not Compress Compressible Characters When Using Document Grid. |
| [setDoNotUseEastAsianBreakRules(boolean value)](#setDoNotUseEastAsianBreakRules-boolean-) | Do Not Compress Compressible Characters When Using Document Grid. |
| [getUseWord2002TableStyleRules()](#getUseWord2002TableStyleRules--) | Emulate Word 2002 Table Style Rules. |
| [setUseWord2002TableStyleRules(boolean value)](#setUseWord2002TableStyleRules-boolean-) | Emulate Word 2002 Table Style Rules. |
| [getGrowAutofit()](#getGrowAutofit--) | Allow Tables to AutoFit Into Page Margins. |
| [setGrowAutofit(boolean value)](#setGrowAutofit-boolean-) | Allow Tables to AutoFit Into Page Margins. |
| [getUseNormalStyleForList()](#getUseNormalStyleForList--) | Do Not Automatically Apply List Paragraph Style To Bulleted/Numbered Text. |
| [setUseNormalStyleForList(boolean value)](#setUseNormalStyleForList-boolean-) | Do Not Automatically Apply List Paragraph Style To Bulleted/Numbered Text. |
| [getDoNotUseIndentAsNumberingTabStop()](#getDoNotUseIndentAsNumberingTabStop--) | Ignore Hanging Indent When Creating Tab Stop After Numbering. |
| [setDoNotUseIndentAsNumberingTabStop(boolean value)](#setDoNotUseIndentAsNumberingTabStop-boolean-) | Ignore Hanging Indent When Creating Tab Stop After Numbering. |
| [getUseAltKinsokuLineBreakRules()](#getUseAltKinsokuLineBreakRules--) | Use Alternate Set of East Asian Line Breaking Rules. |
| [setUseAltKinsokuLineBreakRules(boolean value)](#setUseAltKinsokuLineBreakRules-boolean-) | Use Alternate Set of East Asian Line Breaking Rules. |
| [getAllowSpaceOfSameStyleInTable()](#getAllowSpaceOfSameStyleInTable--) | Allow Contextual Spacing of Paragraphs in Tables. |
| [setAllowSpaceOfSameStyleInTable(boolean value)](#setAllowSpaceOfSameStyleInTable-boolean-) | Allow Contextual Spacing of Paragraphs in Tables. |
| [getDoNotSuppressIndentation()](#getDoNotSuppressIndentation--) | Do Not Ignore Floating Objects When Calculating Paragraph Indentation. |
| [setDoNotSuppressIndentation(boolean value)](#setDoNotSuppressIndentation-boolean-) | Do Not Ignore Floating Objects When Calculating Paragraph Indentation. |
| [getDoNotAutofitConstrainedTables()](#getDoNotAutofitConstrainedTables--) | Do Not AutoFit Tables To Fit Next To Wrapped Objects. |
| [setDoNotAutofitConstrainedTables(boolean value)](#setDoNotAutofitConstrainedTables-boolean-) | Do Not AutoFit Tables To Fit Next To Wrapped Objects. |
| [getAutofitToFirstFixedWidthCell()](#getAutofitToFirstFixedWidthCell--) | Allow Table Columns To Exceed Preferred Widths of Constituent Cells. |
| [setAutofitToFirstFixedWidthCell(boolean value)](#setAutofitToFirstFixedWidthCell-boolean-) | Allow Table Columns To Exceed Preferred Widths of Constituent Cells. |
| [getUnderlineTabInNumList()](#getUnderlineTabInNumList--) | Underline Following Character Following Numbering. |
| [setUnderlineTabInNumList(boolean value)](#setUnderlineTabInNumList-boolean-) | Underline Following Character Following Numbering. |
| [getDisplayHangulFixedWidth()](#getDisplayHangulFixedWidth--) | Always Use Fixed Width for Hangul Characters. |
| [setDisplayHangulFixedWidth(boolean value)](#setDisplayHangulFixedWidth-boolean-) | Always Use Fixed Width for Hangul Characters. |
| [getSplitPgBreakAndParaMark()](#getSplitPgBreakAndParaMark--) | Always Move Paragraph Mark to Page after a Page Break. |
| [setSplitPgBreakAndParaMark(boolean value)](#setSplitPgBreakAndParaMark-boolean-) | Always Move Paragraph Mark to Page after a Page Break. |
| [getDoNotVertAlignCellWithSp()](#getDoNotVertAlignCellWithSp--) | Don't Vertically Align Cells Containing Floating Objects. |
| [setDoNotVertAlignCellWithSp(boolean value)](#setDoNotVertAlignCellWithSp-boolean-) | Don't Vertically Align Cells Containing Floating Objects. |
| [getDoNotBreakConstrainedForcedTable()](#getDoNotBreakConstrainedForcedTable--) | Don't Break Table Rows Around Floating Tables. |
| [setDoNotBreakConstrainedForcedTable(boolean value)](#setDoNotBreakConstrainedForcedTable-boolean-) | Don't Break Table Rows Around Floating Tables. |
| [getDoNotVertAlignInTxbx()](#getDoNotVertAlignInTxbx--) | Ignore Vertical Alignment in Textboxes. |
| [setDoNotVertAlignInTxbx(boolean value)](#setDoNotVertAlignInTxbx-boolean-) | Ignore Vertical Alignment in Textboxes. |
| [getUseAnsiKerningPairs()](#getUseAnsiKerningPairs--) | Use ANSI Kerning Pairs from Fonts. |
| [setUseAnsiKerningPairs(boolean value)](#setUseAnsiKerningPairs-boolean-) | Use ANSI Kerning Pairs from Fonts. |
| [getCachedColBalance()](#getCachedColBalance--) | Use Cached Paragraph Information for Column Balancing. |
| [setCachedColBalance(boolean value)](#setCachedColBalance-boolean-) | Use Cached Paragraph Information for Column Balancing. |
| [getUseFELayout()](#getUseFELayout--) | Do Not Bypass East Asian/Complex Script Layout Code. |
| [setUseFELayout(boolean value)](#setUseFELayout-boolean-) | Do Not Bypass East Asian/Complex Script Layout Code. |
| [getOverrideTableStyleFontSizeAndJustification()](#getOverrideTableStyleFontSizeAndJustification--) | Specifies how the style hierarchy of the document is evaluated. |
| [setOverrideTableStyleFontSizeAndJustification(boolean value)](#setOverrideTableStyleFontSizeAndJustification-boolean-) | Specifies how the style hierarchy of the document is evaluated. |
| [getDisableOpenTypeFontFormattingFeatures()](#getDisableOpenTypeFontFormattingFeatures--) |  |
| [setDisableOpenTypeFontFormattingFeatures(boolean value)](#setDisableOpenTypeFontFormattingFeatures-boolean-) |  |
| [getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning()](#getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning--) |  |
| [setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value)](#setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning-boolean-) |  |
| [getUseWord2010TableStyleRules()](#getUseWord2010TableStyleRules--) |  |
| [setUseWord2010TableStyleRules(boolean value)](#setUseWord2010TableStyleRules-boolean-) |  |
| [getUICompat97To2003()](#getUICompat97To2003--) | **True** to disable UI functionality which is not compatible with Word97-2003. |
| [setUICompat97To2003(boolean value)](#setUICompat97To2003-boolean-) | **True** to disable UI functionality which is not compatible with Word97-2003. |
### optimizeFor(int version) {#optimizeFor-int-}
```
public void optimizeFor(int version)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| version | int |  |

### getNoTabHangInd() {#getNoTabHangInd--}
```
public boolean getNoTabHangInd()
```


Do Not Create Custom Tab Stop for Hanging Indent.

**Returns:**
boolean - The corresponding  boolean  value.
### setNoTabHangInd(boolean value) {#setNoTabHangInd-boolean-}
```
public void setNoTabHangInd(boolean value)
```


Do Not Create Custom Tab Stop for Hanging Indent.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getNoSpaceRaiseLower() {#getNoSpaceRaiseLower--}
```
public boolean getNoSpaceRaiseLower()
```


Do Not Increase Line Height for Raised/Lowered Text.

**Returns:**
boolean - The corresponding  boolean  value.
### setNoSpaceRaiseLower(boolean value) {#setNoSpaceRaiseLower-boolean-}
```
public void setNoSpaceRaiseLower(boolean value)
```


Do Not Increase Line Height for Raised/Lowered Text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSuppressSpBfAfterPgBrk() {#getSuppressSpBfAfterPgBrk--}
```
public boolean getSuppressSpBfAfterPgBrk()
```


Do Not Use Space Before On First Line After a Page Break.

**Returns:**
boolean - The corresponding  boolean  value.
### setSuppressSpBfAfterPgBrk(boolean value) {#setSuppressSpBfAfterPgBrk-boolean-}
```
public void setSuppressSpBfAfterPgBrk(boolean value)
```


Do Not Use Space Before On First Line After a Page Break.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getWrapTrailSpaces() {#getWrapTrailSpaces--}
```
public boolean getWrapTrailSpaces()
```


Line Wrap Trailing Spaces.

**Returns:**
boolean - The corresponding  boolean  value.
### setWrapTrailSpaces(boolean value) {#setWrapTrailSpaces-boolean-}
```
public void setWrapTrailSpaces(boolean value)
```


Line Wrap Trailing Spaces.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getPrintColBlack() {#getPrintColBlack--}
```
public boolean getPrintColBlack()
```


Print Colors as Black And White without Dithering.

**Returns:**
boolean - The corresponding  boolean  value.
### setPrintColBlack(boolean value) {#setPrintColBlack-boolean-}
```
public void setPrintColBlack(boolean value)
```


Print Colors as Black And White without Dithering.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getNoColumnBalance() {#getNoColumnBalance--}
```
public boolean getNoColumnBalance()
```


Do Not Balance Text Columns within a Section.

**Returns:**
boolean - The corresponding  boolean  value.
### setNoColumnBalance(boolean value) {#setNoColumnBalance-boolean-}
```
public void setNoColumnBalance(boolean value)
```


Do Not Balance Text Columns within a Section.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getConvMailMergeEsc() {#getConvMailMergeEsc--}
```
public boolean getConvMailMergeEsc()
```


Treat Backslash Quotation Delimiter as Two Quotation Marks.

**Returns:**
boolean - The corresponding  boolean  value.
### setConvMailMergeEsc(boolean value) {#setConvMailMergeEsc-boolean-}
```
public void setConvMailMergeEsc(boolean value)
```


Treat Backslash Quotation Delimiter as Two Quotation Marks.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSuppressTopSpacing() {#getSuppressTopSpacing--}
```
public boolean getSuppressTopSpacing()
```


Ignore Minimum and Exact Line Height for First Line on Page.

**Returns:**
boolean - The corresponding  boolean  value.
### setSuppressTopSpacing(boolean value) {#setSuppressTopSpacing-boolean-}
```
public void setSuppressTopSpacing(boolean value)
```


Ignore Minimum and Exact Line Height for First Line on Page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUseSingleBorderforContiguousCells() {#getUseSingleBorderforContiguousCells--}
```
public boolean getUseSingleBorderforContiguousCells()
```


Use Simplified Rules For Table Border Conflicts.

**Returns:**
boolean - The corresponding  boolean  value.
### setUseSingleBorderforContiguousCells(boolean value) {#setUseSingleBorderforContiguousCells-boolean-}
```
public void setUseSingleBorderforContiguousCells(boolean value)
```


Use Simplified Rules For Table Border Conflicts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getTransparentMetafiles() {#getTransparentMetafiles--}
```
public boolean getTransparentMetafiles()
```


Specifies not to blank the area behind metafile pictures.

**Returns:**
boolean - The corresponding  boolean  value.
### setTransparentMetafiles(boolean value) {#setTransparentMetafiles-boolean-}
```
public void setTransparentMetafiles(boolean value)
```


Specifies not to blank the area behind metafile pictures.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getShowBreaksInFrames() {#getShowBreaksInFrames--}
```
public boolean getShowBreaksInFrames()
```


Display Page/Column Breaks Present in Frames.

**Returns:**
boolean - The corresponding  boolean  value.
### setShowBreaksInFrames(boolean value) {#setShowBreaksInFrames-boolean-}
```
public void setShowBreaksInFrames(boolean value)
```


Display Page/Column Breaks Present in Frames.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSwapBordersFacingPgs() {#getSwapBordersFacingPgs--}
```
public boolean getSwapBordersFacingPgs()
```


Swap Paragraph Borders on Odd Numbered Pages.

**Returns:**
boolean - The corresponding  boolean  value.
### setSwapBordersFacingPgs(boolean value) {#setSwapBordersFacingPgs-boolean-}
```
public void setSwapBordersFacingPgs(boolean value)
```


Swap Paragraph Borders on Odd Numbered Pages.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotLeaveBackslashAlone() {#getDoNotLeaveBackslashAlone--}
```
public boolean getDoNotLeaveBackslashAlone()
```


Convert Backslash To Yen Sign When Entered.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotLeaveBackslashAlone(boolean value) {#setDoNotLeaveBackslashAlone-boolean-}
```
public void setDoNotLeaveBackslashAlone(boolean value)
```


Convert Backslash To Yen Sign When Entered.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotExpandShiftReturn() {#getDoNotExpandShiftReturn--}
```
public boolean getDoNotExpandShiftReturn()
```


Don't Justify Lines Ending in Soft Line Break.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotExpandShiftReturn(boolean value) {#setDoNotExpandShiftReturn-boolean-}
```
public void setDoNotExpandShiftReturn(boolean value)
```


Don't Justify Lines Ending in Soft Line Break.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUlTrailSpace() {#getUlTrailSpace--}
```
public boolean getUlTrailSpace()
```


Underline All Trailing Spaces.

**Returns:**
boolean - The corresponding  boolean  value.
### setUlTrailSpace(boolean value) {#setUlTrailSpace-boolean-}
```
public void setUlTrailSpace(boolean value)
```


Underline All Trailing Spaces.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getBalanceSingleByteDoubleByteWidth() {#getBalanceSingleByteDoubleByteWidth--}
```
public boolean getBalanceSingleByteDoubleByteWidth()
```


Balance Single Byte and Double Byte Characters.

**Returns:**
boolean - The corresponding  boolean  value.
### setBalanceSingleByteDoubleByteWidth(boolean value) {#setBalanceSingleByteDoubleByteWidth-boolean-}
```
public void setBalanceSingleByteDoubleByteWidth(boolean value)
```


Balance Single Byte and Double Byte Characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSuppressSpacingAtTopOfPage() {#getSuppressSpacingAtTopOfPage--}
```
public boolean getSuppressSpacingAtTopOfPage()
```


Ignore Minimum Line Height for First Line on Page.

**Returns:**
boolean - The corresponding  boolean  value.
### setSuppressSpacingAtTopOfPage(boolean value) {#setSuppressSpacingAtTopOfPage-boolean-}
```
public void setSuppressSpacingAtTopOfPage(boolean value)
```


Ignore Minimum Line Height for First Line on Page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSpacingInWholePoints() {#getSpacingInWholePoints--}
```
public boolean getSpacingInWholePoints()
```


Only Expand/Condense Text By Whole Points.

**Returns:**
boolean - The corresponding  boolean  value.
### setSpacingInWholePoints(boolean value) {#setSpacingInWholePoints-boolean-}
```
public void setSpacingInWholePoints(boolean value)
```


Only Expand/Condense Text By Whole Points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getPrintBodyTextBeforeHeader() {#getPrintBodyTextBeforeHeader--}
```
public boolean getPrintBodyTextBeforeHeader()
```


Print Body Text before Header/Footer Contents.

**Returns:**
boolean - The corresponding  boolean  value.
### setPrintBodyTextBeforeHeader(boolean value) {#setPrintBodyTextBeforeHeader-boolean-}
```
public void setPrintBodyTextBeforeHeader(boolean value)
```


Print Body Text before Header/Footer Contents.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getNoLeading() {#getNoLeading--}
```
public boolean getNoLeading()
```


Do Not Add Leading Between Lines of Text.

**Returns:**
boolean - The corresponding  boolean  value.
### setNoLeading(boolean value) {#setNoLeading-boolean-}
```
public void setNoLeading(boolean value)
```


Do Not Add Leading Between Lines of Text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSpaceForUL() {#getSpaceForUL--}
```
public boolean getSpaceForUL()
```


Add Additional Space Below Baseline For Underlined East Asian Text.

**Returns:**
boolean - The corresponding  boolean  value.
### setSpaceForUL(boolean value) {#setSpaceForUL-boolean-}
```
public void setSpaceForUL(boolean value)
```


Add Additional Space Below Baseline For Underlined East Asian Text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getMWSmallCaps() {#getMWSmallCaps--}
```
public boolean getMWSmallCaps()
```


Emulate Word 5.x for the Macintosh Small Caps Formatting.

**Returns:**
boolean - The corresponding  boolean  value.
### setMWSmallCaps(boolean value) {#setMWSmallCaps-boolean-}
```
public void setMWSmallCaps(boolean value)
```


Emulate Word 5.x for the Macintosh Small Caps Formatting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSuppressTopSpacingWP() {#getSuppressTopSpacingWP--}
```
public boolean getSuppressTopSpacingWP()
```


Emulate WordPerfect 5.x Line Spacing.

**Returns:**
boolean - The corresponding  boolean  value.
### setSuppressTopSpacingWP(boolean value) {#setSuppressTopSpacingWP-boolean-}
```
public void setSuppressTopSpacingWP(boolean value)
```


Emulate WordPerfect 5.x Line Spacing.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getTruncateFontHeightsLikeWP6() {#getTruncateFontHeightsLikeWP6--}
```
public boolean getTruncateFontHeightsLikeWP6()
```


Emulate WordPerfect 6.x Font Height Calculation.

**Returns:**
boolean - The corresponding  boolean  value.
### setTruncateFontHeightsLikeWP6(boolean value) {#setTruncateFontHeightsLikeWP6-boolean-}
```
public void setTruncateFontHeightsLikeWP6(boolean value)
```


Emulate WordPerfect 6.x Font Height Calculation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSubFontBySize() {#getSubFontBySize--}
```
public boolean getSubFontBySize()
```


Increase Priority Of Font Size During Font Substitution.

**Returns:**
boolean - The corresponding  boolean  value.
### setSubFontBySize(boolean value) {#setSubFontBySize-boolean-}
```
public void setSubFontBySize(boolean value)
```


Increase Priority Of Font Size During Font Substitution.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getLineWrapLikeWord6() {#getLineWrapLikeWord6--}
```
public boolean getLineWrapLikeWord6()
```


Emulate Word 6.0 Line Wrapping for East Asian Text.

**Returns:**
boolean - The corresponding  boolean  value.
### setLineWrapLikeWord6(boolean value) {#setLineWrapLikeWord6-boolean-}
```
public void setLineWrapLikeWord6(boolean value)
```


Emulate Word 6.0 Line Wrapping for East Asian Text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotSuppressParagraphBorders() {#getDoNotSuppressParagraphBorders--}
```
public boolean getDoNotSuppressParagraphBorders()
```


Do Not Suppress Paragraph Borders Next To Frames.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotSuppressParagraphBorders(boolean value) {#setDoNotSuppressParagraphBorders-boolean-}
```
public void setDoNotSuppressParagraphBorders(boolean value)
```


Do Not Suppress Paragraph Borders Next To Frames.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getNoExtraLineSpacing() {#getNoExtraLineSpacing--}
```
public boolean getNoExtraLineSpacing()
```


Do Not Center Content on Lines With Exact Line Height.

**Returns:**
boolean - The corresponding  boolean  value.
### setNoExtraLineSpacing(boolean value) {#setNoExtraLineSpacing-boolean-}
```
public void setNoExtraLineSpacing(boolean value)
```


Do Not Center Content on Lines With Exact Line Height.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSuppressBottomSpacing() {#getSuppressBottomSpacing--}
```
public boolean getSuppressBottomSpacing()
```


Ignore Exact Line Height for Last Line on Page.

**Returns:**
boolean - The corresponding  boolean  value.
### setSuppressBottomSpacing(boolean value) {#setSuppressBottomSpacing-boolean-}
```
public void setSuppressBottomSpacing(boolean value)
```


Ignore Exact Line Height for Last Line on Page.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getWPSpaceWidth() {#getWPSpaceWidth--}
```
public boolean getWPSpaceWidth()
```


Specifies whether to set the width of a space as is done in WordPerfect 5.x.

**Returns:**
boolean - The corresponding  boolean  value.
### setWPSpaceWidth(boolean value) {#setWPSpaceWidth-boolean-}
```
public void setWPSpaceWidth(boolean value)
```


Specifies whether to set the width of a space as is done in WordPerfect 5.x.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getWPJustification() {#getWPJustification--}
```
public boolean getWPJustification()
```


Emulate WordPerfect 6.x Paragraph Justification.

**Returns:**
boolean - The corresponding  boolean  value.
### setWPJustification(boolean value) {#setWPJustification-boolean-}
```
public void setWPJustification(boolean value)
```


Emulate WordPerfect 6.x Paragraph Justification.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUsePrinterMetrics() {#getUsePrinterMetrics--}
```
public boolean getUsePrinterMetrics()
```


Use Printer Metrics To Display Documents. Printer Metrics may differ depending on drivers used. For instance, Windows "Microsoft OpenXPS Class Driver 2" and "Microsoft Print to PDF" provide slightly different metrics. Therefore, the final document's layout may change if this option is enabled.

**Returns:**
boolean - The corresponding  boolean  value.
### setUsePrinterMetrics(boolean value) {#setUsePrinterMetrics-boolean-}
```
public void setUsePrinterMetrics(boolean value)
```


Use Printer Metrics To Display Documents. Printer Metrics may differ depending on drivers used. For instance, Windows "Microsoft OpenXPS Class Driver 2" and "Microsoft Print to PDF" provide slightly different metrics. Therefore, the final document's layout may change if this option is enabled.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getShapeLayoutLikeWW8() {#getShapeLayoutLikeWW8--}
```
public boolean getShapeLayoutLikeWW8()
```


Emulate Word 97 Text Wrapping Around Floating Objects.

**Returns:**
boolean - The corresponding  boolean  value.
### setShapeLayoutLikeWW8(boolean value) {#setShapeLayoutLikeWW8-boolean-}
```
public void setShapeLayoutLikeWW8(boolean value)
```


Emulate Word 97 Text Wrapping Around Floating Objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getFootnoteLayoutLikeWW8() {#getFootnoteLayoutLikeWW8--}
```
public boolean getFootnoteLayoutLikeWW8()
```


Emulate Word 6.x/95/97 Footnote Placement.

**Returns:**
boolean - The corresponding  boolean  value.
### setFootnoteLayoutLikeWW8(boolean value) {#setFootnoteLayoutLikeWW8-boolean-}
```
public void setFootnoteLayoutLikeWW8(boolean value)
```


Emulate Word 6.x/95/97 Footnote Placement.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotUseHTMLParagraphAutoSpacing() {#getDoNotUseHTMLParagraphAutoSpacing--}
```
public boolean getDoNotUseHTMLParagraphAutoSpacing()
```


Use Fixed Paragraph Spacing for HTML Auto Setting.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotUseHTMLParagraphAutoSpacing(boolean value) {#setDoNotUseHTMLParagraphAutoSpacing-boolean-}
```
public void setDoNotUseHTMLParagraphAutoSpacing(boolean value)
```


Use Fixed Paragraph Spacing for HTML Auto Setting.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAdjustLineHeightInTable() {#getAdjustLineHeightInTable--}
```
public boolean getAdjustLineHeightInTable()
```


Add Document Grid Line Pitch To Lines in Table Cells.

**Returns:**
boolean - The corresponding  boolean  value.
### setAdjustLineHeightInTable(boolean value) {#setAdjustLineHeightInTable-boolean-}
```
public void setAdjustLineHeightInTable(boolean value)
```


Add Document Grid Line Pitch To Lines in Table Cells.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getForgetLastTabAlignment() {#getForgetLastTabAlignment--}
```
public boolean getForgetLastTabAlignment()
```


Ignore Width of Last Tab Stop When Aligning Paragraph If It Is Not Left Aligned.

**Returns:**
boolean - The corresponding  boolean  value.
### setForgetLastTabAlignment(boolean value) {#setForgetLastTabAlignment-boolean-}
```
public void setForgetLastTabAlignment(boolean value)
```


Ignore Width of Last Tab Stop When Aligning Paragraph If It Is Not Left Aligned.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAutoSpaceLikeWord95() {#getAutoSpaceLikeWord95--}
```
public boolean getAutoSpaceLikeWord95()
```


Emulate Word 95 Full-Width Character Spacing.

**Returns:**
boolean - The corresponding  boolean  value.
### setAutoSpaceLikeWord95(boolean value) {#setAutoSpaceLikeWord95-boolean-}
```
public void setAutoSpaceLikeWord95(boolean value)
```


Emulate Word 95 Full-Width Character Spacing.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAlignTablesRowByRow() {#getAlignTablesRowByRow--}
```
public boolean getAlignTablesRowByRow()
```


Align Table Rows Independently.

**Returns:**
boolean - The corresponding  boolean  value.
### setAlignTablesRowByRow(boolean value) {#setAlignTablesRowByRow-boolean-}
```
public void setAlignTablesRowByRow(boolean value)
```


Align Table Rows Independently.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getLayoutRawTableWidth() {#getLayoutRawTableWidth--}
```
public boolean getLayoutRawTableWidth()
```


Ignore Space Before Table When Deciding If Table Should Wrap Floating Object.

**Returns:**
boolean - The corresponding  boolean  value.
### setLayoutRawTableWidth(boolean value) {#setLayoutRawTableWidth-boolean-}
```
public void setLayoutRawTableWidth(boolean value)
```


Ignore Space Before Table When Deciding If Table Should Wrap Floating Object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getLayoutTableRowsApart() {#getLayoutTableRowsApart--}
```
public boolean getLayoutTableRowsApart()
```


Allow Table Rows to Wrap Inline Objects Independently.

**Returns:**
boolean - The corresponding  boolean  value.
### setLayoutTableRowsApart(boolean value) {#setLayoutTableRowsApart-boolean-}
```
public void setLayoutTableRowsApart(boolean value)
```


Allow Table Rows to Wrap Inline Objects Independently.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUseWord97LineBreakRules() {#getUseWord97LineBreakRules--}
```
public boolean getUseWord97LineBreakRules()
```


Emulate Word 97 East Asian Line Breaking.

**Returns:**
boolean - The corresponding  boolean  value.
### setUseWord97LineBreakRules(boolean value) {#setUseWord97LineBreakRules-boolean-}
```
public void setUseWord97LineBreakRules(boolean value)
```


Emulate Word 97 East Asian Line Breaking.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotBreakWrappedTables() {#getDoNotBreakWrappedTables--}
```
public boolean getDoNotBreakWrappedTables()
```


Do Not Allow Floating Tables To Break Across Pages.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotBreakWrappedTables(boolean value) {#setDoNotBreakWrappedTables-boolean-}
```
public void setDoNotBreakWrappedTables(boolean value)
```


Do Not Allow Floating Tables To Break Across Pages.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotSnapToGridInCell() {#getDoNotSnapToGridInCell--}
```
public boolean getDoNotSnapToGridInCell()
```


Do Not Snap to Document Grid in Table Cells with Objects.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotSnapToGridInCell(boolean value) {#setDoNotSnapToGridInCell-boolean-}
```
public void setDoNotSnapToGridInCell(boolean value)
```


Do Not Snap to Document Grid in Table Cells with Objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSelectFldWithFirstOrLastChar() {#getSelectFldWithFirstOrLastChar--}
```
public boolean getSelectFldWithFirstOrLastChar()
```


Select Field When First or Last Character Is Selected.

**Returns:**
boolean - The corresponding  boolean  value.
### setSelectFldWithFirstOrLastChar(boolean value) {#setSelectFldWithFirstOrLastChar-boolean-}
```
public void setSelectFldWithFirstOrLastChar(boolean value)
```


Select Field When First or Last Character Is Selected.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getApplyBreakingRules() {#getApplyBreakingRules--}
```
public boolean getApplyBreakingRules()
```


Use Legacy Ethiopic and Amharic Line Breaking Rules.

**Returns:**
boolean - The corresponding  boolean  value.
### setApplyBreakingRules(boolean value) {#setApplyBreakingRules-boolean-}
```
public void setApplyBreakingRules(boolean value)
```


Use Legacy Ethiopic and Amharic Line Breaking Rules.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotWrapTextWithPunct() {#getDoNotWrapTextWithPunct--}
```
public boolean getDoNotWrapTextWithPunct()
```


Do Not Allow Hanging Punctuation With Character Grid.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotWrapTextWithPunct(boolean value) {#setDoNotWrapTextWithPunct-boolean-}
```
public void setDoNotWrapTextWithPunct(boolean value)
```


Do Not Allow Hanging Punctuation With Character Grid.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotUseEastAsianBreakRules() {#getDoNotUseEastAsianBreakRules--}
```
public boolean getDoNotUseEastAsianBreakRules()
```


Do Not Compress Compressible Characters When Using Document Grid.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotUseEastAsianBreakRules(boolean value) {#setDoNotUseEastAsianBreakRules-boolean-}
```
public void setDoNotUseEastAsianBreakRules(boolean value)
```


Do Not Compress Compressible Characters When Using Document Grid.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUseWord2002TableStyleRules() {#getUseWord2002TableStyleRules--}
```
public boolean getUseWord2002TableStyleRules()
```


Emulate Word 2002 Table Style Rules.

**Returns:**
boolean - The corresponding  boolean  value.
### setUseWord2002TableStyleRules(boolean value) {#setUseWord2002TableStyleRules-boolean-}
```
public void setUseWord2002TableStyleRules(boolean value)
```


Emulate Word 2002 Table Style Rules.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getGrowAutofit() {#getGrowAutofit--}
```
public boolean getGrowAutofit()
```


Allow Tables to AutoFit Into Page Margins.

**Returns:**
boolean - The corresponding  boolean  value.
### setGrowAutofit(boolean value) {#setGrowAutofit-boolean-}
```
public void setGrowAutofit(boolean value)
```


Allow Tables to AutoFit Into Page Margins.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUseNormalStyleForList() {#getUseNormalStyleForList--}
```
public boolean getUseNormalStyleForList()
```


Do Not Automatically Apply List Paragraph Style To Bulleted/Numbered Text.

**Returns:**
boolean - The corresponding  boolean  value.
### setUseNormalStyleForList(boolean value) {#setUseNormalStyleForList-boolean-}
```
public void setUseNormalStyleForList(boolean value)
```


Do Not Automatically Apply List Paragraph Style To Bulleted/Numbered Text.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotUseIndentAsNumberingTabStop() {#getDoNotUseIndentAsNumberingTabStop--}
```
public boolean getDoNotUseIndentAsNumberingTabStop()
```


Ignore Hanging Indent When Creating Tab Stop After Numbering.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotUseIndentAsNumberingTabStop(boolean value) {#setDoNotUseIndentAsNumberingTabStop-boolean-}
```
public void setDoNotUseIndentAsNumberingTabStop(boolean value)
```


Ignore Hanging Indent When Creating Tab Stop After Numbering.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUseAltKinsokuLineBreakRules() {#getUseAltKinsokuLineBreakRules--}
```
public boolean getUseAltKinsokuLineBreakRules()
```


Use Alternate Set of East Asian Line Breaking Rules.

**Returns:**
boolean - The corresponding  boolean  value.
### setUseAltKinsokuLineBreakRules(boolean value) {#setUseAltKinsokuLineBreakRules-boolean-}
```
public void setUseAltKinsokuLineBreakRules(boolean value)
```


Use Alternate Set of East Asian Line Breaking Rules.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAllowSpaceOfSameStyleInTable() {#getAllowSpaceOfSameStyleInTable--}
```
public boolean getAllowSpaceOfSameStyleInTable()
```


Allow Contextual Spacing of Paragraphs in Tables.

**Returns:**
boolean - The corresponding  boolean  value.
### setAllowSpaceOfSameStyleInTable(boolean value) {#setAllowSpaceOfSameStyleInTable-boolean-}
```
public void setAllowSpaceOfSameStyleInTable(boolean value)
```


Allow Contextual Spacing of Paragraphs in Tables.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotSuppressIndentation() {#getDoNotSuppressIndentation--}
```
public boolean getDoNotSuppressIndentation()
```


Do Not Ignore Floating Objects When Calculating Paragraph Indentation.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotSuppressIndentation(boolean value) {#setDoNotSuppressIndentation-boolean-}
```
public void setDoNotSuppressIndentation(boolean value)
```


Do Not Ignore Floating Objects When Calculating Paragraph Indentation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotAutofitConstrainedTables() {#getDoNotAutofitConstrainedTables--}
```
public boolean getDoNotAutofitConstrainedTables()
```


Do Not AutoFit Tables To Fit Next To Wrapped Objects.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotAutofitConstrainedTables(boolean value) {#setDoNotAutofitConstrainedTables-boolean-}
```
public void setDoNotAutofitConstrainedTables(boolean value)
```


Do Not AutoFit Tables To Fit Next To Wrapped Objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getAutofitToFirstFixedWidthCell() {#getAutofitToFirstFixedWidthCell--}
```
public boolean getAutofitToFirstFixedWidthCell()
```


Allow Table Columns To Exceed Preferred Widths of Constituent Cells. The option is called "Use Word 2003 table autofit rules" in MS Word 2013 user interface. It actually affects how the grid is calculated for fixed layout tables, too (for some cases).

**Returns:**
boolean - The corresponding  boolean  value.
### setAutofitToFirstFixedWidthCell(boolean value) {#setAutofitToFirstFixedWidthCell-boolean-}
```
public void setAutofitToFirstFixedWidthCell(boolean value)
```


Allow Table Columns To Exceed Preferred Widths of Constituent Cells. The option is called "Use Word 2003 table autofit rules" in MS Word 2013 user interface. It actually affects how the grid is calculated for fixed layout tables, too (for some cases).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUnderlineTabInNumList() {#getUnderlineTabInNumList--}
```
public boolean getUnderlineTabInNumList()
```


Underline Following Character Following Numbering.

**Returns:**
boolean - The corresponding  boolean  value.
### setUnderlineTabInNumList(boolean value) {#setUnderlineTabInNumList-boolean-}
```
public void setUnderlineTabInNumList(boolean value)
```


Underline Following Character Following Numbering.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDisplayHangulFixedWidth() {#getDisplayHangulFixedWidth--}
```
public boolean getDisplayHangulFixedWidth()
```


Always Use Fixed Width for Hangul Characters.

**Returns:**
boolean - The corresponding  boolean  value.
### setDisplayHangulFixedWidth(boolean value) {#setDisplayHangulFixedWidth-boolean-}
```
public void setDisplayHangulFixedWidth(boolean value)
```


Always Use Fixed Width for Hangul Characters.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getSplitPgBreakAndParaMark() {#getSplitPgBreakAndParaMark--}
```
public boolean getSplitPgBreakAndParaMark()
```


Always Move Paragraph Mark to Page after a Page Break.

**Returns:**
boolean - The corresponding  boolean  value.
### setSplitPgBreakAndParaMark(boolean value) {#setSplitPgBreakAndParaMark-boolean-}
```
public void setSplitPgBreakAndParaMark(boolean value)
```


Always Move Paragraph Mark to Page after a Page Break.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotVertAlignCellWithSp() {#getDoNotVertAlignCellWithSp--}
```
public boolean getDoNotVertAlignCellWithSp()
```


Don't Vertically Align Cells Containing Floating Objects.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotVertAlignCellWithSp(boolean value) {#setDoNotVertAlignCellWithSp-boolean-}
```
public void setDoNotVertAlignCellWithSp(boolean value)
```


Don't Vertically Align Cells Containing Floating Objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotBreakConstrainedForcedTable() {#getDoNotBreakConstrainedForcedTable--}
```
public boolean getDoNotBreakConstrainedForcedTable()
```


Don't Break Table Rows Around Floating Tables.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotBreakConstrainedForcedTable(boolean value) {#setDoNotBreakConstrainedForcedTable-boolean-}
```
public void setDoNotBreakConstrainedForcedTable(boolean value)
```


Don't Break Table Rows Around Floating Tables.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDoNotVertAlignInTxbx() {#getDoNotVertAlignInTxbx--}
```
public boolean getDoNotVertAlignInTxbx()
```


Ignore Vertical Alignment in Textboxes.

**Returns:**
boolean - The corresponding  boolean  value.
### setDoNotVertAlignInTxbx(boolean value) {#setDoNotVertAlignInTxbx-boolean-}
```
public void setDoNotVertAlignInTxbx(boolean value)
```


Ignore Vertical Alignment in Textboxes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUseAnsiKerningPairs() {#getUseAnsiKerningPairs--}
```
public boolean getUseAnsiKerningPairs()
```


Use ANSI Kerning Pairs from Fonts.

**Returns:**
boolean - The corresponding  boolean  value.
### setUseAnsiKerningPairs(boolean value) {#setUseAnsiKerningPairs-boolean-}
```
public void setUseAnsiKerningPairs(boolean value)
```


Use ANSI Kerning Pairs from Fonts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getCachedColBalance() {#getCachedColBalance--}
```
public boolean getCachedColBalance()
```


Use Cached Paragraph Information for Column Balancing.

**Returns:**
boolean - The corresponding  boolean  value.
### setCachedColBalance(boolean value) {#setCachedColBalance-boolean-}
```
public void setCachedColBalance(boolean value)
```


Use Cached Paragraph Information for Column Balancing.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getUseFELayout() {#getUseFELayout--}
```
public boolean getUseFELayout()
```


Do Not Bypass East Asian/Complex Script Layout Code.

**Returns:**
boolean - The corresponding  boolean  value.
### setUseFELayout(boolean value) {#setUseFELayout-boolean-}
```
public void setUseFELayout(boolean value)
```


Do Not Bypass East Asian/Complex Script Layout Code.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getOverrideTableStyleFontSizeAndJustification() {#getOverrideTableStyleFontSizeAndJustification--}
```
public boolean getOverrideTableStyleFontSizeAndJustification()
```


Specifies how the style hierarchy of the document is evaluated.

**Returns:**
boolean - The corresponding  boolean  value.
### setOverrideTableStyleFontSizeAndJustification(boolean value) {#setOverrideTableStyleFontSizeAndJustification-boolean-}
```
public void setOverrideTableStyleFontSizeAndJustification(boolean value)
```


Specifies how the style hierarchy of the document is evaluated.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### getDisableOpenTypeFontFormattingFeatures() {#getDisableOpenTypeFontFormattingFeatures--}
```
public boolean getDisableOpenTypeFontFormattingFeatures()
```




**Returns:**
boolean
### setDisableOpenTypeFontFormattingFeatures(boolean value) {#setDisableOpenTypeFontFormattingFeatures-boolean-}
```
public void setDisableOpenTypeFontFormattingFeatures(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning() {#getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning--}
```
public boolean getSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning()
```




**Returns:**
boolean
### setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value) {#setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning-boolean-}
```
public void setSwapInsideAndOutsideForMirrorIndentsAndRelativePositioning(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getUseWord2010TableStyleRules() {#getUseWord2010TableStyleRules--}
```
public boolean getUseWord2010TableStyleRules()
```




**Returns:**
boolean
### setUseWord2010TableStyleRules(boolean value) {#setUseWord2010TableStyleRules-boolean-}
```
public void setUseWord2010TableStyleRules(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getUICompat97To2003() {#getUICompat97To2003--}
```
public boolean getUICompat97To2003()
```


**True** to disable UI functionality which is not compatible with Word97-2003. Default value is **false**. Controls the Word97-2003 compatibility setting that disables UI functionality which is not compatible with Word97-2003. When **true**, 'w:uiCompat97To2003' XML element is written to '\\word\\settings.xml' document package part. Default value is **false**. When set to **false**, this element is not written. Technically this property is not part of compatibility options, but we have put it here for API convenience.

**Returns:**
boolean - The corresponding  boolean  value.
### setUICompat97To2003(boolean value) {#setUICompat97To2003-boolean-}
```
public void setUICompat97To2003(boolean value)
```


**True** to disable UI functionality which is not compatible with Word97-2003. Default value is **false**. Controls the Word97-2003 compatibility setting that disables UI functionality which is not compatible with Word97-2003. When **true**, 'w:uiCompat97To2003' XML element is written to '\\word\\settings.xml' document package part. Default value is **false**. When set to **false**, this element is not written. Technically this property is not part of compatibility options, but we have put it here for API convenience.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

