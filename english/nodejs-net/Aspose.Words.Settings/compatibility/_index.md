---
title: Compatibility enumeration
linktitle: Compatibility enumeration
articleTitle: Compatibility enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Settings.Compatibility enumeration. Specifies names of compatibility options."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Settings/compatibility/
---

## Compatibility enumeration

Specifies names of compatibility options.


### Members

| Name | Description |
| --- | --- |
| NoTabHangInd | No Tab Hang Indent |
| NoSpaceRaiseLower | No Space Raise Lower |
| SuppressSpBfAfterPgBrk | Suppress Space Before Paragraph Break |
| WrapTrailSpaces | Wrap Trailing Spaces |
| PrintColBlack | Print Column Background |
| NoColumnBalance | No Column Balancing |
| ConvMailMergeEsc | Convert Mail Merge Escapes |
| SuppressTopSpacing | Suppress Top Spacing |
| UseSingleBorderforContiguousCells | Use Single Border for Contiguous Cells |
| TransparentMetafiles | Transparent Metafiles |
| ShowBreaksInFrames | Show Breaks in Frames |
| SwapBordersOddFacingPgs | Swap Borders on Odd-Facing Pages |
| DoNotLeaveBackslashAlone | Do Not Leave Backslash Alone |
| DoNotExpandOnShiftReturn | Do Not Expand on Shift Return |
| UlTrailSpace | Underline Trailing Space |
| BalanceSingleByteDoubleByteWidth | Balance Single-Byte and Double-Byte Widths |
| SuppressTopSpacingAtTopOfPage | Suppress Top Line Spacing in WordPerfect |
| SpacingInWholePoints | Spacing in Whole Points |
| PrintBodyTextBeforeHeader | Print Body Text Before Header |
| NoLeading | No Leading |
| SpaceForUL | Space for Underline |
| MWSmallCaps | MW Small Caps |
| SuppressTopLineSpacingWP | Suppress Top Line Spacing in WordPerfect |
| TruncateFontHeightLikeWP6 | Truncate Font Height Like WordPerfect 6 |
| SubFontBySize | Substitute Font by Size |
| LineWrapLikeWord6 | Line Wrap Like Word 6 |
| DoNotSuppressParagraphBorder | Do Not Suppress Paragraph Border |
| NoExtraLineSpacing | No Extra Line Spacing |
| SuppressBottomSpacing | Suppress Bottom Spacing |
| WPSpaceWidth | WordPerfect Space Width |
| WPJustification | WordPerfect Justification |
| UsePrinterMetrics | Use Printer Metrics |
| ShapeLayoutLikeWW8 | Shape Layout Like Word 2000 |
| FootnoteLayoutLikeWW8 | Footnote Layout Like Word 2000 |
| DoNotUseHtmlParagraphAutoSpacing | Do Not Use HTML Paragraph Auto Spacing |
| AdjustLineHeightInTable | Adjust Line Height in Table |
| ForgetLastTabAlignment | Forget Last Tab Alignment |
| AutoSpaceLikeWord95 | Auto Space Like Word 95 |
| AlignTableRowByRow | Align Table Rows by Rule |
| LayoutRawTableWidth | Layout Raw Table Width |
| LayoutTableRowsApart | Layout Table Rows Apart |
| UseWord97LineBreakRules | Use Word 97 Line Break Rules |
| DoNotBreakWrappedTables | Do Not Break Wrapped Tables |
| doNotSnapToGridInCell | Do Not Snap to Grid in Cells |
| SelectFldWithFirstOrLastChar | Select Field with First or Last Character |
| ApplyBreakingRules | Apply Breaking Rules |
| DoNotWrapTextWithPunct | Do Not Wrap Text with Punctuation |
| DoNotUseEastAsianBreakRules | Do Not Use East Asian Break Rules |
| UseWord2002TableStyleRules | Use Word 2002 Table Style Rules |
| GrowAutofit | Grow AutoFit |
| UseNormalStyleForList | Use Normal Style for List |
| DoNotUseIndentAsNumberingTabStop | Do Not Use Indent as Numbering Tab Stop |
| UseAltKinsokuLineBreakRules | Use Alt Kinsoku Line Break Rules |
| AllowSpaceOfSameStyleInTable | Allow Space of Same Style in Table |
| DoNotSuppressIndentation | Do Not Suppress Indentation |
| DoNotAutofitConstrainedTables | Do Not AutoFit Constrained Tables |
| AutofitToFirstFixedWidthCell | AutoFit to First Fixed-Width Cell |
| UnderlineTabInNumList | Underline Tab in Numbered List |
| DisplayHangulFixedWidth | Display Hangul Fixed Width |
| SplitPgBreakAndParaMark | Split Page Break and Paragraph Mark |
| DoNotVertAlignCellWithSp | Do Not Vertically Align Cell with Spacing |
| DoNotBreakConstrainedForcedTable | Do Not Break Constrained Forced Tables |
| DoNotVertAlignInTxbx | Do Not Vertically Align in Textboxes |
| UseAnsiKerningPairs | Use ANSI Kerning Pairs |
| CachedColBalance | Cached Column Balancing |
| UseFELayout | Use Far East Layout |
| UICompat97To2003 | User Interface Compatibility Mode from Word 97 to Word 2003 |
| OverrideTableStyleFontSizeAndJustification | Override Table Style Font Size and Justification |
| DisableOpenTypeFontFormattingFeatures | Disable OpenType Font Formatting Features |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | Swap Inside and Outside for Mirror Indents and Relative Positioning |
| UseWord2010TableStyleRules | Use Word 2010 Table Style Rules |

### Examples

Shows how to optimize the document for different versions of Microsoft Word.

```js
test('OptimizeFor', () => {
  let doc = new aw.Document();

  // This object contains an extensive list of flags unique to each document
  // that allow us to facilitate backward compatibility with older versions of Microsoft Word.
  let options = doc.compatibilityOptions;

  // Print the default settings for a blank document.
  console.log("\nDefault optimization settings:");
  printCompatibilityOptions(options);

  // We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
  doc.save(base.artifactsDir + "CompatibilityOptions.optimizeFor.DefaultSettings.docx");

  // We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
  doc.compatibilityOptions.optimizeFor(aw.Settings.MsWordVersion.Word2010);
  console.log("\nOptimized for Word 2010:");
  printCompatibilityOptions(options);

  doc.compatibilityOptions.optimizeFor(aw.Settings.MsWordVersion.Word2000);
  console.log("\nOptimized for Word 2000:");
  printCompatibilityOptions(options);
});


/// <summary>
/// Groups all flags in a document's compatibility options object by state, then prints each group.
/// </summary>
function printCompatibilityOptions(options) {
  let enabledOptions = [];
  let disabledOptions = [];
  addOptionName(options.adjustLineHeightInTable, "AdjustLineHeightInTable", enabledOptions, disabledOptions);
  addOptionName(options.alignTablesRowByRow, "AlignTablesRowByRow", enabledOptions, disabledOptions);
  addOptionName(options.allowSpaceOfSameStyleInTable, "AllowSpaceOfSameStyleInTable", enabledOptions, disabledOptions);
  addOptionName(options.applyBreakingRules, "ApplyBreakingRules", enabledOptions, disabledOptions);
  addOptionName(options.autoSpaceLikeWord95, "AutoSpaceLikeWord95", enabledOptions, disabledOptions);
  addOptionName(options.autofitToFirstFixedWidthCell, "AutofitToFirstFixedWidthCell", enabledOptions, disabledOptions);
  addOptionName(options.balanceSingleByteDoubleByteWidth, "BalanceSingleByteDoubleByteWidth", enabledOptions, disabledOptions);
  addOptionName(options.cachedColBalance, "CachedColBalance", enabledOptions, disabledOptions);
  addOptionName(options.convMailMergeEsc, "ConvMailMergeEsc", enabledOptions, disabledOptions);
  addOptionName(options.disableOpenTypeFontFormattingFeatures, "DisableOpenTypeFontFormattingFeatures", enabledOptions, disabledOptions);
  addOptionName(options.displayHangulFixedWidth, "DisplayHangulFixedWidth", enabledOptions, disabledOptions);
  addOptionName(options.doNotAutofitConstrainedTables, "DoNotAutofitConstrainedTables", enabledOptions, disabledOptions);
  addOptionName(options.doNotBreakConstrainedForcedTable, "DoNotBreakConstrainedForcedTable", enabledOptions, disabledOptions);
  addOptionName(options.doNotBreakWrappedTables, "DoNotBreakWrappedTables", enabledOptions, disabledOptions);
  addOptionName(options.doNotExpandShiftReturn, "DoNotExpandShiftReturn", enabledOptions, disabledOptions);
  addOptionName(options.doNotLeaveBackslashAlone, "DoNotLeaveBackslashAlone", enabledOptions, disabledOptions);
  addOptionName(options.doNotSnapToGridInCell, "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
  addOptionName(options.doNotSuppressIndentation, "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
  addOptionName(options.doNotSuppressParagraphBorders, "DoNotSuppressParagraphBorders", enabledOptions, disabledOptions);
  addOptionName(options.doNotUseEastAsianBreakRules, "DoNotUseEastAsianBreakRules", enabledOptions, disabledOptions);
  addOptionName(options.doNotUseHTMLParagraphAutoSpacing, "DoNotUseHTMLParagraphAutoSpacing", enabledOptions, disabledOptions);
  addOptionName(options.doNotUseIndentAsNumberingTabStop, "DoNotUseIndentAsNumberingTabStop", enabledOptions, disabledOptions);
  addOptionName(options.doNotVertAlignCellWithSp, "DoNotVertAlignCellWithSp", enabledOptions, disabledOptions);
  addOptionName(options.doNotVertAlignInTxbx, "DoNotVertAlignInTxbx", enabledOptions, disabledOptions);
  addOptionName(options.doNotWrapTextWithPunct, "DoNotWrapTextWithPunct", enabledOptions, disabledOptions);
  addOptionName(options.footnoteLayoutLikeWW8, "FootnoteLayoutLikeWW8", enabledOptions, disabledOptions);
  addOptionName(options.forgetLastTabAlignment, "ForgetLastTabAlignment", enabledOptions, disabledOptions);
  addOptionName(options.growAutofit, "GrowAutofit", enabledOptions, disabledOptions);
  addOptionName(options.layoutRawTableWidth, "LayoutRawTableWidth", enabledOptions, disabledOptions);
  addOptionName(options.layoutTableRowsApart, "LayoutTableRowsApart", enabledOptions, disabledOptions);
  addOptionName(options.lineWrapLikeWord6, "LineWrapLikeWord6", enabledOptions, disabledOptions);
  addOptionName(options.mWSmallCaps, "MWSmallCaps", enabledOptions, disabledOptions);
  addOptionName(options.noColumnBalance, "NoColumnBalance", enabledOptions, disabledOptions);
  addOptionName(options.noExtraLineSpacing, "NoExtraLineSpacing", enabledOptions, disabledOptions);
  addOptionName(options.noLeading, "NoLeading", enabledOptions, disabledOptions);
  addOptionName(options.noSpaceRaiseLower, "NoSpaceRaiseLower", enabledOptions, disabledOptions);
  addOptionName(options.noTabHangInd, "NoTabHangInd", enabledOptions, disabledOptions);
  addOptionName(options.overrideTableStyleFontSizeAndJustification, "OverrideTableStyleFontSizeAndJustification", enabledOptions, disabledOptions);
  addOptionName(options.printBodyTextBeforeHeader, "PrintBodyTextBeforeHeader", enabledOptions, disabledOptions);
  addOptionName(options.printColBlack, "PrintColBlack", enabledOptions, disabledOptions);
  addOptionName(options.selectFldWithFirstOrLastChar, "SelectFldWithFirstOrLastChar", enabledOptions, disabledOptions);
  addOptionName(options.shapeLayoutLikeWW8, "ShapeLayoutLikeWW8", enabledOptions, disabledOptions);
  addOptionName(options.showBreaksInFrames, "ShowBreaksInFrames", enabledOptions, disabledOptions);
  addOptionName(options.spaceForUL, "SpaceForUL", enabledOptions, disabledOptions);
  addOptionName(options.spacingInWholePoints, "SpacingInWholePoints", enabledOptions, disabledOptions);
  addOptionName(options.splitPgBreakAndParaMark, "SplitPgBreakAndParaMark", enabledOptions, disabledOptions);
  addOptionName(options.subFontBySize, "SubFontBySize", enabledOptions, disabledOptions);
  addOptionName(options.suppressBottomSpacing, "SuppressBottomSpacing", enabledOptions, disabledOptions);
  addOptionName(options.suppressSpBfAfterPgBrk, "SuppressSpBfAfterPgBrk", enabledOptions, disabledOptions);
  addOptionName(options.suppressSpacingAtTopOfPage, "SuppressSpacingAtTopOfPage", enabledOptions, disabledOptions);
  addOptionName(options.suppressTopSpacing, "SuppressTopSpacing", enabledOptions, disabledOptions);
  addOptionName(options.suppressTopSpacingWP, "SuppressTopSpacingWP", enabledOptions, disabledOptions);
  addOptionName(options.swapBordersFacingPgs, "SwapBordersFacingPgs", enabledOptions, disabledOptions);
  addOptionName(options.swapInsideAndOutsideForMirrorIndentsAndRelativePositioning, "SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning", enabledOptions, disabledOptions);
  addOptionName(options.transparentMetafiles, "TransparentMetafiles", enabledOptions, disabledOptions);
  addOptionName(options.truncateFontHeightsLikeWP6, "TruncateFontHeightsLikeWP6", enabledOptions, disabledOptions);
  addOptionName(options.uICompat97To2003, "UICompat97To2003", enabledOptions, disabledOptions);
  addOptionName(options.ulTrailSpace, "UlTrailSpace", enabledOptions, disabledOptions);
  addOptionName(options.underlineTabInNumList, "UnderlineTabInNumList", enabledOptions, disabledOptions);
  addOptionName(options.useAltKinsokuLineBreakRules, "UseAltKinsokuLineBreakRules", enabledOptions, disabledOptions);
  addOptionName(options.useAnsiKerningPairs, "UseAnsiKerningPairs", enabledOptions, disabledOptions);
  addOptionName(options.useFELayout, "UseFELayout", enabledOptions, disabledOptions);
  addOptionName(options.useNormalStyleForList, "UseNormalStyleForList", enabledOptions, disabledOptions);
  addOptionName(options.usePrinterMetrics, "UsePrinterMetrics", enabledOptions, disabledOptions);
  addOptionName(options.useSingleBorderforContiguousCells, "UseSingleBorderforContiguousCells", enabledOptions, disabledOptions);
  addOptionName(options.useWord2002TableStyleRules, "UseWord2002TableStyleRules", enabledOptions, disabledOptions);
  addOptionName(options.useWord2010TableStyleRules, "UseWord2010TableStyleRules", enabledOptions, disabledOptions);
  addOptionName(options.useWord97LineBreakRules, "UseWord97LineBreakRules", enabledOptions, disabledOptions);
  addOptionName(options.wPJustification, "WPJustification", enabledOptions, disabledOptions);
  addOptionName(options.wPSpaceWidth, "WPSpaceWidth", enabledOptions, disabledOptions);
  addOptionName(options.wrapTrailSpaces, "WrapTrailSpaces", enabledOptions, disabledOptions);
  /*console.log("\tEnabled options:");
  for (let optionName of enabledOptions)
    console.log(`\t\t${optionName}`);
  console.log("\tDisabled options:");
  for (let optionName of disabledOptions)
    console.log(`\t\t${optionName}`);*/
}

function addOptionName(option, optionName, enabledOptions, disabledOptions)
{
  if (option)
    enabledOptions.push(optionName);
  else
    disabledOptions.push(optionName);
}
```

### See Also

* module [Aspose.Words.Settings](../)

