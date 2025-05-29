---
title: Compatibility Enum
linktitle: Compatibility
articleTitle: Compatibility
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.Settings.Compatibility per sbloccare potenti opzioni di compatibilità per un'elaborazione fluida dei documenti e prestazioni migliorate.
type: docs
weight: 6600
url: /it/net/aspose.words.settings/compatibility/
---
## Compatibility enumeration

Specifica i nomi delle opzioni di compatibilità.

```csharp
public enum Compatibility
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| NoTabHangInd | `0` | Nessuna tabulazione indentata |
| NoSpaceRaiseLower | `1` | Nessuno spazio Alza Abbassa |
| SuppressSpBfAfterPgBrk | `2` | Sopprimi spazio prima dell'interruzione di paragrafo |
| WrapTrailSpaces | `3` | Avvolgi spazi finali |
| PrintColBlack | `4` | Stampa sfondo colonna |
| NoColumnBalance | `5` | Nessun bilanciamento delle colonne |
| ConvMailMergeEsc | `6` | Converti escape per la stampa unione |
| SuppressTopSpacing | `7` | Sopprimi spaziatura superiore |
| UseSingleBorderforContiguousCells | `8` | Usa bordo singolo per celle contigue |
| TransparentMetafiles | `9` | Metafile trasparenti |
| ShowBreaksInFrames | `10` | Mostra interruzioni nei frame |
| SwapBordersOddFacingPgs | `11` | Scambia i bordi nelle pagine con pagine dispari |
| DoNotLeaveBackslashAlone | `12` | Non lasciare la barra rovesciata da sola |
| DoNotExpandOnShiftReturn | `13` | Non espandere durante il ritorno a capo |
| UlTrailSpace | `14` | Sottolinea lo spazio finale |
| BalanceSingleByteDoubleByteWidth | `15` | Bilanciare le larghezze a byte singolo e doppio byte |
| SuppressTopSpacingAtTopOfPage | `16` | Elimina la spaziatura della riga superiore in WordPerfect |
| SpacingInWholePoints | `17` | Spaziatura in punti interi |
| PrintBodyTextBeforeHeader | `18` | Stampa il corpo del testo prima dell'intestazione |
| NoLeading | `19` | Nessun leader |
| SpaceForUL | `20` | Spazio per sottolineare |
| MWSmallCaps | `21` | MW Small Caps |
| SuppressTopLineSpacingWP | `22` | Elimina la spaziatura della riga superiore in WordPerfect |
| TruncateFontHeightLikeWP6 | `23` | Tronca l'altezza del carattere come WordPerfect 6 |
| SubFontBySize | `24` | Sostituisci il carattere per dimensione |
| LineWrapLikeWord6 | `25` | A capo automatico come Word 6 |
| DoNotSuppressParagraphBorder | `26` | Non sopprimere il bordo del paragrafo |
| NoExtraLineSpacing | `27` | Nessuna spaziatura di linea aggiuntiva |
| SuppressBottomSpacing | `28` | Sopprimi spaziatura inferiore |
| WPSpaceWidth | `29` | Larghezza spazio WordPerfect |
| WPJustification | `30` | Giustificazione di WordPerfect |
| UsePrinterMetrics | `31` | Utilizza le metriche della stampante |
| ShapeLayoutLikeWW8 | `32` | Layout della forma come Word 2000 |
| FootnoteLayoutLikeWW8 | `33` | Layout delle note a piè di pagina come Word 2000 |
| DoNotUseHtmlParagraphAutoSpacing | `34` | Non utilizzare la spaziatura automatica dei paragrafi HTML |
| AdjustLineHeightInTable | `35` | Regola l'altezza della riga nella tabella |
| ForgetLastTabAlignment | `36` | Dimentica l'allineamento dell'ultima scheda |
| AutoSpaceLikeWord95 | `37` | Spazio automatico come Word 95 |
| AlignTableRowByRow | `38` | Allinea le righe della tabella con la regola |
| LayoutRawTableWidth | `39` | Larghezza tabella grezza layout |
| LayoutTableRowsApart | `40` | Righe della tabella di layout separate |
| UseWord97LineBreakRules | `41` | Usa le regole di interruzione di riga di Word 97 |
| DoNotBreakWrappedTables | `42` | Non interrompere le tabelle wrappate |
| doNotSnapToGridInCell | `43` | Non agganciare alla griglia nelle celle |
| SelectFldWithFirstOrLastChar | `44` | Seleziona campo con primo o ultimo carattere |
| ApplyBreakingRules | `45` | Applica le regole di infrazione |
| DoNotWrapTextWithPunct | `46` | Non racchiudere il testo con la punteggiatura |
| DoNotUseEastAsianBreakRules | `47` | Non usare le regole di rottura dell'Asia orientale |
| UseWord2002TableStyleRules | `48` | Usa le regole di stile tabella di Word 2002 |
| GrowAutofit | `49` | Aumenta Adattamento automatico |
| UseNormalStyleForList | `50` | Usa lo stile normale per List |
| DoNotUseIndentAsNumberingTabStop | `51` | Non utilizzare il rientro come tabulazione di numerazione |
| UseAltKinsokuLineBreakRules | `52` | Usa le regole di interruzione di riga di Alt Kinsoku |
| AllowSpaceOfSameStyleInTable | `53` | Consenti spazio dello stesso stile nella tabella |
| DoNotSuppressIndentation | `54` | Non sopprimere l'indentazione |
| DoNotAutofitConstrainedTables | `55` | Non adattare automaticamente le tabelle vincolate |
| AutofitToFirstFixedWidthCell | `56` | Adatta automaticamente alla prima cella a larghezza fissa |
| UnderlineTabInNumList | `57` | Sottolinea tabulazione in elenco numerato |
| DisplayHangulFixedWidth | `58` | Visualizza Hangul a larghezza fissa |
| SplitPgBreakAndParaMark | `59` | Interruzione di pagina e segno di paragrafo divisi |
| DoNotVertAlignCellWithSp | `60` | Non allineare verticalmente la cella con la spaziatura |
| DoNotBreakConstrainedForcedTable | `61` | Non interrompere le tabelle forzate vincolate |
| DoNotVertAlignInTxbx | `62` | Non allineare verticalmente nelle caselle di testo |
| UseAnsiKerningPairs | `63` | Usa coppie di kerning ANSI |
| CachedColBalance | `64` | Bilanciamento delle colonne memorizzate nella cache |
| UseFELayout | `65` | Usa il layout Estremo Oriente |
| UICompat97To2003 | `66` | Modalità di compatibilità dell'interfaccia utente da Word 97 a Word 2003 |
| OverrideTableStyleFontSizeAndJustification | `67` | Sostituisci la dimensione del carattere e la giustificazione dello stile della tabella |
| DisableOpenTypeFontFormattingFeatures | `68` | Disabilita le funzionalità di formattazione dei font OpenType |
| SwapInsideAndOutsideForMirrorIndentsAndRelativePositioning | `69` | Scambia interno ed esterno per rientri speculari e posizionamento relativo |
| UseWord2010TableStyleRules | `70` | Usa le regole di stile tabella di Word 2010 |

## Esempi

Mostra come ottimizzare il documento per diverse versioni di Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Questo oggetto contiene un elenco esteso di flag univoci per ciascun documento
    // che ci consentono di facilitare la compatibilità con le versioni precedenti di Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Stampa le impostazioni predefinite per un documento vuoto.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Possiamo accedere a queste impostazioni in Microsoft Word tramite "File" -> "Opzioni" -> "Avanzate" -> "Opzioni di compatibilità per...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Possiamo utilizzare il metodo OptimizeFor per garantire la compatibilità ottimale con una versione specifica di Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Raggruppa tutti i flag nell'oggetto delle opzioni di compatibilità di un documento in base allo stato, quindi stampa ciascun gruppo.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Settings](../../aspose.words.settings/)
* assemblea [Aspose.Words](../../)
