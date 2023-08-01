---
title: Compatibility Enum
linktitle: Compatibility
articleTitle: Compatibility
second_title: Aspose.Words for .NET
description: Aspose.Words.Settings.Compatibility enum. Specifies names of compatibility options in C#.
type: docs
weight: 5750
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
| NoTabHangInd | `0` |  |
| NoSpaceRaiseLower | `1` |  |
| SuppressSpBfAfterPgBrk | `2` |  |
| WrapTrailSpaces | `3` |  |
| PrintColBlack | `4` |  |
| NoColumnBalance | `5` |  |
| ConvMailMergeEsc | `6` |  |
| SuppressTopSpacing | `7` |  |
| UseSingleBorderforContiguousCells | `8` |  |
| TransparentMetafiles | `9` |  |
| ShowBreaksInFrames | `10` |  |
| SwapBordersOddFacingPgs | `11` |  |
| DoNotLeaveBackslashAlone | `12` |  |
| DoNotExpandOnShiftReturn | `13` |  |
| UlTrailSpace | `14` |  |
| BalanceSingleByteDoubleByteWidth | `15` |  |
| SuppressTopSpacingAtTopOfPage | `16` |  |
| SpacingInWholePoints | `17` |  |
| PrintBodyTextBeforeHeader | `18` |  |
| NoLeading | `19` |  |
| SpaceForUL | `20` |  |
| MWSmallCaps | `21` |  |
| SuppressTopLineSpacingWP | `22` |  |
| TruncateFontHeightLikeWP6 | `23` |  |
| SubFontBySize | `24` |  |
| LineWrapLikeWord6 | `25` |  |
| DoNotSuppressParagraphBorder | `26` |  |
| NoExtraLineSpacing | `27` |  |
| SuppressBottomSpacing | `28` |  |
| WPSpaceWidth | `29` |  |
| WPJustification | `30` |  |
| UsePrinterMetrics | `31` |  |
| ShapeLayoutLikeWW8 | `32` |  |
| FootnoteLayoutLikeWW8 | `33` |  |
| DoNotUseHtmlParagraphAutoSpacing | `34` |  |
| AdjustLineHeightInTable | `35` |  |
| ForgetLastTabAlignment | `36` |  |
| AutoSpaceLikeWord95 | `37` |  |
| AlignTableRowByRow | `38` |  |
| LayoutRawTableWidth | `39` |  |
| LayoutTableRowsApart | `40` |  |
| UseWord97LineBreakRules | `41` |  |
| DoNotBreakWrappedTables | `42` |  |
| doNotSnapToGridInCell | `43` |  |
| SelectFldWithFirstOrLastChar | `44` |  |
| ApplyBreakingRules | `45` |  |
| DoNotWrapTextWithPunct | `46` |  |
| DoNotUseEastAsianBreakRules | `47` |  |
| UseWord2002TableStyleRules | `48` |  |
| GrowAutofit | `49` |  |
| UseNormalStyleForList | `50` |  |
| DoNotUseIndentAsNumberingTabStop | `51` |  |
| UseAltKinsokuLineBreakRules | `52` |  |
| AllowSpaceOfSameStyleInTable | `53` |  |
| DoNotSuppressIndentation | `54` |  |
| DoNotAutofitConstrainedTables | `55` |  |
| AutofitToFirstFixedWidthCell | `56` |  |
| UnderlineTabInNumList | `57` |  |
| DisplayHangulFixedWidth | `58` |  |
| SplitPgBreakAndParaMark | `59` |  |
| DoNotVertAlignCellWithSp | `60` |  |
| DoNotBreakConstrainedForcedTable | `61` |  |
| DoNotVertAlignInTxbx | `62` |  |
| UseAnsiKerningPairs | `63` |  |
| CachedColBalance | `64` |  |
| UseFELayout | `65` |  |
| UICompat97To2003 | `66` |  |
| OverrideTableStyleFontSizeAndJustification | `67` |  |
| DisableOpenTypeFontFormattingFeatures | `68` |  |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | `69` |  |
| UseWord2010TableStyleRules | `70` |  |

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
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### See Also

* namespace [Aspose.Words.Settings](../../aspose.words.settings/)
* assembly [Aspose.Words](../../)
