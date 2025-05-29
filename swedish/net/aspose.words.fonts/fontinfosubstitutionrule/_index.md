---
title: FontInfoSubstitutionRule Class
linktitle: FontInfoSubstitutionRule
articleTitle: FontInfoSubstitutionRule
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fonts.FontInfoSubstitutionRule för att optimera teckensnittshanteringen i dina dokument med sömlösa ersättningsmöjligheter.
type: docs
weight: 3370
url: /sv/net/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class

Regel för ersättning av teckensnittsinformation.

För att lära dig mer, besök[Arbeta med teckensnitt](https://docs.aspose.com/words/net/working-with-fonts/) dokumentationsartikel.

```csharp
public class FontInfoSubstitutionRule : FontSubstitutionRule
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Anger om regeln är aktiverad eller inte. |

## Anmärkningar

Enligt denna regel utvärderar Aspose.Words alla relaterade fält i[`FontInfo`](../fontinfo/) (Panose, Sig etc.) for det saknade teckensnittet och hittar den närmaste matchningen bland de tillgängliga teckensnittskällorna.[`FontInfo`](../fontinfo/) är inte tillgängligt för det saknade teckensnittet kommer ingenting att göras.

## Exempel

Visar hur man ställer in egenskapen för att hitta den närmaste matchningen för ett saknat teckensnitt från de tillgängliga teckensnittskällorna.

```csharp
public void EnableFontSubstitution()
{
    // Öppna ett dokument som innehåller text formaterad med ett teckensnitt som inte finns i någon av våra teckensnittskällor.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Tilldela en återanropning för att hantera varningar om teckensnittsersättning.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Ange ett standardnamn för teckensnitt och aktivera teckensnittsersättning.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Ursprungliga teckensnittsmått bör användas efter teckensnittsersättning.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Vi får en varning om teckensnittsersättning om vi sparar ett dokument med ett saknat teckensnitt.
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // Vi kan också verifiera varningar i samlingen och rensa dem.
    Assert.AreEqual(WarningSource.Layout, substitutionWarningHandler.FontWarnings[0].Source);
    Assert.AreEqual(
        "Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
        substitutionWarningHandler.FontWarnings[0].Description);

    substitutionWarningHandler.FontWarnings.Clear();

    Assert.AreEqual(0, substitutionWarningHandler.FontWarnings.Count);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Anropas varje gång en varning uppstår under inläsning/sparning.
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### Se även

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* namnutrymme [Aspose.Words.Fonts](../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../)
