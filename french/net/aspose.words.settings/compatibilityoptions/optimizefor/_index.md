---
title: CompatibilityOptions.OptimizeFor
linktitle: OptimizeFor
articleTitle: OptimizeFor
second_title: Aspose.Words pour .NET
description: Améliorez vos documents avec la méthode OptimizeFor dans CompatibilityOptions. Adaptez le comportement d'Aspose.Words à des versions spécifiques de MS Word pour des résultats optimaux.
type: docs
weight: 720
url: /fr/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Permet d'optimiser le contenu du document ainsi que le comportement par défaut d'Aspose.Words pour une version particulière de MS Word.

Utilisez cette méthode pour empêcher MS Word d'afficher le ruban « Mode de compatibilité » lors du chargement du document. (Notez que vous devrez peut-être également définir le[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) propriété to Iso29500_2008_Transitional ou supérieur.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

## Exemples

Montre comment aligner verticalement le contenu textuel d'une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Définissez la propriété « VerticalAnchor » sur « TextBoxAnchor.Top » pour
// alignez le texte dans cette zone de texte avec le côté supérieur de la forme.
// Définissez la propriété « VerticalAnchor » sur « TextBoxAnchor.Middle » pour
// alignez le texte de cette zone de texte au centre de la forme.
// Définissez la propriété « VerticalAnchor » sur « TextBoxAnchor.Bottom » pour
// alignez le texte de cette zone de texte sur le bas de la forme.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// L'alignement vertical du texte à l'intérieur des zones de texte est disponible à partir de Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Montre comment définir une spécification de conformité OOXML à laquelle un document enregistré doit adhérer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous configurons les options de compatibilité pour être conformes à Microsoft Word 2003,
// l'insertion d'une image définira sa forme à l'aide de VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// La norme OOXML « ISO/IEC 29500:2008 » ne prend pas en charge les formes VML.
// Si nous définissons la propriété « Compliance » de l'objet SaveOptions sur « OoxmlCompliance.Iso29500_2008_Strict »,
 // tout document que nous sauvegardons en passant cet objet devra suivre cette norme.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme à l'aide de DML pour adhérer à la norme OOXML « ISO/IEC 29500:2008 ».
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

Montre comment optimiser le document pour différentes versions de Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Cet objet contient une longue liste d'indicateurs uniques à chaque document
    // qui nous permettent de faciliter la compatibilité descendante avec les anciennes versions de Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Imprimez les paramètres par défaut pour un document vierge.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Nous pouvons accéder à ces paramètres dans Microsoft Word via "Fichier" -> "Options" -> "Avancé" -> "Options de compatibilité pour...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Nous pouvons utiliser la méthode OptimizeFor pour assurer une compatibilité optimale avec une version spécifique de Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Regroupe tous les indicateurs dans l'objet d'options de compatibilité d'un document par état, puis imprime chaque groupe.
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

### Voir également

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* espace de noms [Aspose.Words.Settings](../../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../../)
