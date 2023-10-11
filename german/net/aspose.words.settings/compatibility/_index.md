---
title: Enum Compatibility
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Settings.Compatibility opsomming. Gibt Namen von Kompatibilitätsoptionen an.
type: docs
weight: 5770
url: /de/net/aspose.words.settings/compatibility/
---
## Compatibility enumeration

Gibt Namen von Kompatibilitätsoptionen an.

```csharp
public enum Compatibility
```

### Werte

| Name | Wert | Beschreibung |
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

### Beispiele

Zeigt, wie das Dokument für verschiedene Versionen von Microsoft Word optimiert wird.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Dieses Objekt enthält eine umfangreiche Liste von Flags, die für jedes Dokument einzigartig sind
    // die es uns ermöglichen, die Abwärtskompatibilität mit älteren Versionen von Microsoft Word zu erleichtern.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Standardeinstellungen für ein leeres Dokument drucken.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Auf diese Einstellungen können wir in Microsoft Word über „Datei“ -> zugreifen. „Optionen“ -> „Erweitert“ –> „Kompatibilitätsoptionen für…“.
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Wir können die OptimizeFor-Methode verwenden, um eine optimale Kompatibilität mit einer bestimmten Microsoft Word-Version sicherzustellen.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Gruppiert alle Flags in den Kompatibilitätsoptionen eines Dokuments nach Status und gibt dann jede Gruppe aus.
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

### Siehe auch

* namensraum [Aspose.Words.Settings](../../aspose.words.settings/)
* Montage [Aspose.Words](../../)


