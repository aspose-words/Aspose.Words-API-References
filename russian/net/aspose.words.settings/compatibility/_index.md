---
title: Compatibility
second_title: Справочник по API Aspose.Words для .NET
description: Указывает имена параметров совместимости.
type: docs
weight: 5430
url: /ru/net/aspose.words.settings/compatibility/
---
## Compatibility enumeration

Указывает имена параметров совместимости.

```csharp
public enum Compatibility
```

### Ценности

| Имя | Ценность | Описание |
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

### Примеры

Показывает, как оптимизировать документ для разных версий Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

     // Этот объект содержит обширный список флагов, уникальных для каждого document
     // это позволяет нам обеспечить обратную совместимость со старыми версиями Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

     // Печать настроек по умолчанию для пустого документа.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

     // Мы можем получить доступ к этим настройкам в Microsoft Word через «Файл» -> "Опции" -> «Дополнительно» -> "Параметры совместимости для...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

     // Мы можем использовать метод OptimizeFor для обеспечения оптимальной совместимости с определенной версией Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
 /// Группирует все флаги в объекте параметров совместимости документа по состоянию, затем печатает каждую группу.
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

### Смотрите также

* namespace [Aspose.Words.Settings](../../aspose.words.settings)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
