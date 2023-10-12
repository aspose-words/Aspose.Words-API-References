---
title: Enum WarningType
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.WarningType uppräkning. Anger typen av varning som utfärdas av Aspose.Words under dokumentladdning eller sparande.
type: docs
weight: 6660
url: /sv/net/aspose.words/warningtype/
---
## WarningType enumeration

Anger typen av varning som utfärdas av Aspose.Words under dokumentladdning eller sparande.

```csharp
[Flags]
public enum WarningType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| DataLossCategory | `FF` | Viss text/char/bild eller annan data kommer att saknas antingen i dokumentträdet efter laddning, eller från det skapade dokumentet efter save. |
| DataLoss | `1` | Generisk dataförlust, ingen specifik kod. |
| MajorFormattingLossCategory | `FF00` | Det resulterande dokumentet eller en viss plats i det kan se väsentligt annorlunda ut jämfört med originaldokumentet. |
| MajorFormattingLoss | `100` | Generisk stor formateringsförlust, ingen specifik kod. |
| MinorFormattingLossCategory | `FF0000` | Det resulterande dokumentet eller en viss plats i det kan se något annorlunda ut jämfört med från originaldokumentet. |
| MinorFormattingLoss | `10000` | Generisk mindre formateringsförlust, ingen specifik kod. |
| FontSubstitution | `20000` | Teckensnittet har ersatts. |
| FontEmbedding | `40000` | Förlust av inbäddad teckensnittsinformation under dokumentsparande. |
| UnexpectedContentCategory | `F000000` | En del innehåll i källdokumentet kunde inte kännas igen (dvs. stöds inte), detta kan eller kanske inte orsaka problem eller resultera i data-/formateringsförlust. |
| UnexpectedContent | `1000000` | Generiskt oväntat innehåll, ingen specifik kod. |
| Hint | `10000000` | ger råd om ett potentiellt problem eller föreslår en förbättring. |

### Exempel

Visar hur du ställer in egenskapen för att hitta den närmaste matchningen för ett saknat teckensnitt från tillgängliga teckensnittskällor.

```csharp
public void EnableFontSubstitution()
{
    // Öppna ett dokument som innehåller text formaterad med ett teckensnitt som inte finns i någon av våra teckensnittskällor.
    Document doc = new Document(MyDir + "Missing font.docx");

    // Tilldela en återuppringning för hantering av varningar för teckensnittsersättning.
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // Ange ett standardtypsnittsnamn och aktivera teckensnittsersättning.
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // Original teckensnittsmått bör användas efter teckensnittsersättning.
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // Vi kommer att få en varning för ersättning av teckensnitt om vi sparar ett dokument med ett teckensnitt som saknas.
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

    Assert.That(substitutionWarningHandler.FontWarnings, Is.Empty);
}

public class HandleDocumentSubstitutionWarnings : IWarningCallback
{
    /// <summary>
    /// Anropas varje gång en varning inträffar under laddning/sparning.
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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


