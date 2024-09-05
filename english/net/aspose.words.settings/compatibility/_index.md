---
title: Compatibility Enum
linktitle: Compatibility
articleTitle: Compatibility
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.Compatibility enum. Specifies names of compatibility options in C#.
type: docs
weight: 6160
url: /net/aspose.words.settings/compatibility/
---
## Compatibility enumeration

Specifies names of compatibility options.

```csharp
public enum Compatibility
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| NoTabHangInd | `0` | No Tab Hang Indent |
| NoSpaceRaiseLower | `1` | No Space Raise Lower |
| SuppressSpBfAfterPgBrk | `2` | Suppress Space Before Paragraph Break |
| WrapTrailSpaces | `3` | Wrap Trailing Spaces |
| PrintColBlack | `4` | Print Column Background |
| NoColumnBalance | `5` | No Column Balancing |
| ConvMailMergeEsc | `6` | Convert Mail Merge Escapes |
| SuppressTopSpacing | `7` | Suppress Top Spacing |
| UseSingleBorderforContiguousCells | `8` | Use Single Border for Contiguous Cells |
| TransparentMetafiles | `9` | Transparent Metafiles |
| ShowBreaksInFrames | `10` | Show Breaks in Frames |
| SwapBordersOddFacingPgs | `11` | Swap Borders on Odd-Facing Pages |
| DoNotLeaveBackslashAlone | `12` | Do Not Leave Backslash Alone |
| DoNotExpandOnShiftReturn | `13` | Do Not Expand on Shift Return |
| UlTrailSpace | `14` | Underline Trailing Space |
| BalanceSingleByteDoubleByteWidth | `15` | Balance Single-Byte and Double-Byte Widths |
| SuppressTopSpacingAtTopOfPage | `16` | Suppress Top Line Spacing in WordPerfect |
| SpacingInWholePoints | `17` | Spacing in Whole Points |
| PrintBodyTextBeforeHeader | `18` | Print Body Text Before Header |
| NoLeading | `19` | No Leading |
| SpaceForUL | `20` | Space for Underline |
| MWSmallCaps | `21` | MW Small Caps |
| SuppressTopLineSpacingWP | `22` | Suppress Top Line Spacing in WordPerfect |
| TruncateFontHeightLikeWP6 | `23` | Truncate Font Height Like WordPerfect 6 |
| SubFontBySize | `24` | Substitute Font by Size |
| LineWrapLikeWord6 | `25` | Line Wrap Like Word 6 |
| DoNotSuppressParagraphBorder | `26` | Do Not Suppress Paragraph Border |
| NoExtraLineSpacing | `27` | No Extra Line Spacing |
| SuppressBottomSpacing | `28` | Suppress Bottom Spacing |
| WPSpaceWidth | `29` | WordPerfect Space Width |
| WPJustification | `30` | WordPerfect Justification |
| UsePrinterMetrics | `31` | Use Printer Metrics |
| ShapeLayoutLikeWW8 | `32` | Shape Layout Like Word 2000 |
| FootnoteLayoutLikeWW8 | `33` | Footnote Layout Like Word 2000 |
| DoNotUseHtmlParagraphAutoSpacing | `34` | Do Not Use HTML Paragraph Auto Spacing |
| AdjustLineHeightInTable | `35` | Adjust Line Height in Table |
| ForgetLastTabAlignment | `36` | Forget Last Tab Alignment |
| AutoSpaceLikeWord95 | `37` | Auto Space Like Word 95 |
| AlignTableRowByRow | `38` | Align Table Rows by Rule |
| LayoutRawTableWidth | `39` | Layout Raw Table Width |
| LayoutTableRowsApart | `40` | Layout Table Rows Apart |
| UseWord97LineBreakRules | `41` | Use Word 97 Line Break Rules |
| DoNotBreakWrappedTables | `42` | Do Not Break Wrapped Tables |
| doNotSnapToGridInCell | `43` | Do Not Snap to Grid in Cells |
| SelectFldWithFirstOrLastChar | `44` | Select Field with First or Last Character |
| ApplyBreakingRules | `45` | Apply Breaking Rules |
| DoNotWrapTextWithPunct | `46` | Do Not Wrap Text with Punctuation |
| DoNotUseEastAsianBreakRules | `47` | Do Not Use East Asian Break Rules |
| UseWord2002TableStyleRules | `48` | Use Word 2002 Table Style Rules |
| GrowAutofit | `49` | Grow AutoFit |
| UseNormalStyleForList | `50` | Use Normal Style for List |
| DoNotUseIndentAsNumberingTabStop | `51` | Do Not Use Indent as Numbering Tab Stop |
| UseAltKinsokuLineBreakRules | `52` | Use Alt Kinsoku Line Break Rules |
| AllowSpaceOfSameStyleInTable | `53` | Allow Space of Same Style in Table |
| DoNotSuppressIndentation | `54` | Do Not Suppress Indentation |
| DoNotAutofitConstrainedTables | `55` | Do Not AutoFit Constrained Tables |
| AutofitToFirstFixedWidthCell | `56` | AutoFit to First Fixed-Width Cell |
| UnderlineTabInNumList | `57` | Underline Tab in Numbered List |
| DisplayHangulFixedWidth | `58` | Display Hangul Fixed Width |
| SplitPgBreakAndParaMark | `59` | Split Page Break and Paragraph Mark |
| DoNotVertAlignCellWithSp | `60` | Do Not Vertically Align Cell with Spacing |
| DoNotBreakConstrainedForcedTable | `61` | Do Not Break Constrained Forced Tables |
| DoNotVertAlignInTxbx | `62` | Do Not Vertically Align in Textboxes |
| UseAnsiKerningPairs | `63` | Use ANSI Kerning Pairs |
| CachedColBalance | `64` | Cached Column Balancing |
| UseFELayout | `65` | Use Far East Layout |
| UICompat97To2003 | `66` | User Interface Compatibility Mode from Word 97 to Word 2003 |
| OverrideTableStyleFontSizeAndJustification | `67` | Override Table Style Font Size and Justification |
| DisableOpenTypeFontFormattingFeatures | `68` | Disable OpenType Font Formatting Features |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | `69` | Swap Inside and Outside for Mirror Indents and Relative Positioning |
| UseWord2010TableStyleRules | `70` | Use Word 2010 Table Style Rules |

## Examples

Shows how to optimize the document for different versions of Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // This object contains an extensive list of flags unique to each document
    // that allow us to facilitate backward compatibility with older versions of Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Print the default settings for a blank document.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Groups all flags in a document's compatibility options object by state, then prints each group.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    IList<string> enabledOptions = new List<string>();
    IList<string> disabledOptions = new List<string>();
    AddOptionName(options.AdjustLineHeightInTable, "AdjustLineHeightInTable", enabledOptions, disabledOptions);
    AddOptionName(options.AlignTablesRowByRow, "AlignTablesRowByRow", enabledOptions, disabledOptions);
    AddOptionName(options.AllowSpaceOfSameStyleInTable, "AllowSpaceOfSameStyleInTable", enabledOptions, disabledOptions);
    AddOptionName(options.ApplyBreakingRules, "ApplyBreakingRules", enabledOptions, disabledOptions);
    AddOptionName(options.AutoSpaceLikeWord95, "AutoSpaceLikeWord95", enabledOptions, disabledOptions);
    AddOptionName(options.AutofitToFirstFixedWidthCell, "AutofitToFirstFixedWidthCell", enabledOptions, disabledOptions);
    AddOptionName(options.BalanceSingleByteDoubleByteWidth, "BalanceSingleByteDoubleByteWidth", enabledOptions, disabledOptions);
    AddOptionName(options.CachedColBalance, "CachedColBalance", enabledOptions, disabledOptions);
    AddOptionName(options.ConvMailMergeEsc, "ConvMailMergeEsc", enabledOptions, disabledOptions);
    AddOptionName(options.DisableOpenTypeFontFormattingFeatures, "DisableOpenTypeFontFormattingFeatures", enabledOptions, disabledOptions);
    AddOptionName(options.DisplayHangulFixedWidth, "DisplayHangulFixedWidth", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotAutofitConstrainedTables, "DoNotAutofitConstrainedTables", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotBreakConstrainedForcedTable, "DoNotBreakConstrainedForcedTable", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotBreakWrappedTables, "DoNotBreakWrappedTables", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotExpandShiftReturn, "DoNotExpandShiftReturn", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotLeaveBackslashAlone, "DoNotLeaveBackslashAlone", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotSnapToGridInCell, "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotSuppressIndentation, "DoNotSnapToGridInCell", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotSuppressParagraphBorders, "DoNotSuppressParagraphBorders", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotUseEastAsianBreakRules, "DoNotUseEastAsianBreakRules", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotUseHTMLParagraphAutoSpacing, "DoNotUseHTMLParagraphAutoSpacing", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotUseIndentAsNumberingTabStop, "DoNotUseIndentAsNumberingTabStop", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotVertAlignCellWithSp, "DoNotVertAlignCellWithSp", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotVertAlignInTxbx, "DoNotVertAlignInTxbx", enabledOptions, disabledOptions);
    AddOptionName(options.DoNotWrapTextWithPunct, "DoNotWrapTextWithPunct", enabledOptions, disabledOptions);
    AddOptionName(options.FootnoteLayoutLikeWW8, "FootnoteLayoutLikeWW8", enabledOptions, disabledOptions);
    AddOptionName(options.ForgetLastTabAlignment, "ForgetLastTabAlignment", enabledOptions, disabledOptions);
    AddOptionName(options.GrowAutofit, "GrowAutofit", enabledOptions, disabledOptions);
    AddOptionName(options.LayoutRawTableWidth, "LayoutRawTableWidth", enabledOptions, disabledOptions);
    AddOptionName(options.LayoutTableRowsApart, "LayoutTableRowsApart", enabledOptions, disabledOptions);
    AddOptionName(options.LineWrapLikeWord6, "LineWrapLikeWord6", enabledOptions, disabledOptions);
    AddOptionName(options.MWSmallCaps, "MWSmallCaps", enabledOptions, disabledOptions);
    AddOptionName(options.NoColumnBalance, "NoColumnBalance", enabledOptions, disabledOptions);
    AddOptionName(options.NoExtraLineSpacing, "NoExtraLineSpacing", enabledOptions, disabledOptions);
    AddOptionName(options.NoLeading, "NoLeading", enabledOptions, disabledOptions);
    AddOptionName(options.NoSpaceRaiseLower, "NoSpaceRaiseLower", enabledOptions, disabledOptions);
    AddOptionName(options.NoTabHangInd, "NoTabHangInd", enabledOptions, disabledOptions);
    AddOptionName(options.OverrideTableStyleFontSizeAndJustification, "OverrideTableStyleFontSizeAndJustification", enabledOptions, disabledOptions);
    AddOptionName(options.PrintBodyTextBeforeHeader, "PrintBodyTextBeforeHeader", enabledOptions, disabledOptions);
    AddOptionName(options.PrintColBlack, "PrintColBlack", enabledOptions, disabledOptions);
    AddOptionName(options.SelectFldWithFirstOrLastChar, "SelectFldWithFirstOrLastChar", enabledOptions, disabledOptions);
    AddOptionName(options.ShapeLayoutLikeWW8, "ShapeLayoutLikeWW8", enabledOptions, disabledOptions);
    AddOptionName(options.ShowBreaksInFrames, "ShowBreaksInFrames", enabledOptions, disabledOptions);
    AddOptionName(options.SpaceForUL, "SpaceForUL", enabledOptions, disabledOptions);
    AddOptionName(options.SpacingInWholePoints, "SpacingInWholePoints", enabledOptions, disabledOptions);
    AddOptionName(options.SplitPgBreakAndParaMark, "SplitPgBreakAndParaMark", enabledOptions, disabledOptions);
    AddOptionName(options.SubFontBySize, "SubFontBySize", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressBottomSpacing, "SuppressBottomSpacing", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressSpBfAfterPgBrk, "SuppressSpBfAfterPgBrk", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressSpacingAtTopOfPage, "SuppressSpacingAtTopOfPage", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressTopSpacing, "SuppressTopSpacing", enabledOptions, disabledOptions);
    AddOptionName(options.SuppressTopSpacingWP, "SuppressTopSpacingWP", enabledOptions, disabledOptions);
    AddOptionName(options.SwapBordersFacingPgs, "SwapBordersFacingPgs", enabledOptions, disabledOptions);
    AddOptionName(options.SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning, "SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning", enabledOptions, disabledOptions);
    AddOptionName(options.TransparentMetafiles, "TransparentMetafiles", enabledOptions, disabledOptions);
    AddOptionName(options.TruncateFontHeightsLikeWP6, "TruncateFontHeightsLikeWP6", enabledOptions, disabledOptions);
    AddOptionName(options.UICompat97To2003, "UICompat97To2003", enabledOptions, disabledOptions);
    AddOptionName(options.UlTrailSpace, "UlTrailSpace", enabledOptions, disabledOptions);
    AddOptionName(options.UnderlineTabInNumList, "UnderlineTabInNumList", enabledOptions, disabledOptions);
    AddOptionName(options.UseAltKinsokuLineBreakRules, "UseAltKinsokuLineBreakRules", enabledOptions, disabledOptions);
    AddOptionName(options.UseAnsiKerningPairs, "UseAnsiKerningPairs", enabledOptions, disabledOptions);
    AddOptionName(options.UseFELayout, "UseFELayout", enabledOptions, disabledOptions);
    AddOptionName(options.UseNormalStyleForList, "UseNormalStyleForList", enabledOptions, disabledOptions);
    AddOptionName(options.UsePrinterMetrics, "UsePrinterMetrics", enabledOptions, disabledOptions);
    AddOptionName(options.UseSingleBorderforContiguousCells, "UseSingleBorderforContiguousCells", enabledOptions, disabledOptions);
    AddOptionName(options.UseWord2002TableStyleRules, "UseWord2002TableStyleRules", enabledOptions, disabledOptions);
    AddOptionName(options.UseWord2010TableStyleRules, "UseWord2010TableStyleRules", enabledOptions, disabledOptions);
    AddOptionName(options.UseWord97LineBreakRules, "UseWord97LineBreakRules", enabledOptions, disabledOptions);
    AddOptionName(options.WPJustification, "WPJustification", enabledOptions, disabledOptions);
    AddOptionName(options.WPSpaceWidth, "WPSpaceWidth", enabledOptions, disabledOptions);
    AddOptionName(options.WrapTrailSpaces, "WrapTrailSpaces", enabledOptions, disabledOptions);
    Console.WriteLine("\tEnabled options:");
    foreach (string optionName in enabledOptions)
        Console.WriteLine($"\t\t{optionName}");
    Console.WriteLine("\tDisabled options:");
    foreach (string optionName in disabledOptions)
        Console.WriteLine($"\t\t{optionName}");
}

private static void AddOptionName(Boolean option, String optionName, IList<string> enabledOptions, IList<string> disabledOptions)
{
    if (option)
        enabledOptions.Add(optionName);
    else
        disabledOptions.Add(optionName);
}
```

### See Also

* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
