---
title: Compatibility
second_title: Referencia de API de Aspose.Words para .NET
description: Especifica los nombres de las opciones de compatibilidad.
type: docs
weight: 5480
url: /es/net/aspose.words.settings/compatibility/
---
## Compatibility enumeration

Especifica los nombres de las opciones de compatibilidad.

```csharp
public enum Compatibility
```

### Valores

| Nombre | Valor | Descripción |
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

### Ejemplos

Muestra cómo optimizar el documento para diferentes versiones de Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Este objeto contiene una extensa lista de banderas únicas para cada documento
    // que nos permiten facilitar la retrocompatibilidad con versiones anteriores de Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Imprime la configuración predeterminada para un documento en blanco.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Podemos acceder a esta configuración en Microsoft Word a través de "Archivo" -> "Opciones" -> "Avanzado" -> "Opciones de compatibilidad para...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Podemos usar el método OptimizeFor para garantizar una compatibilidad óptima con una versión específica de Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Agrupa todas las banderas en el objeto de opciones de compatibilidad de un documento por estado, luego imprime cada grupo.
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

### Ver también

* espacio de nombres [Aspose.Words.Settings](../../aspose.words.settings)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
