---
title: WarningType Enum
linktitle: WarningType
articleTitle: WarningType
second_title: Aspose.Words för .NET
description: Upptäck enumereringen Aspose.Words.WarningType, som kategoriserar varningar vid inläsning eller sparning av dokument, vilket förbättrar din dokumenthanteringsupplevelse.
type: docs
weight: 7510
url: /sv/net/aspose.words/warningtype/
---
## WarningType enumeration

Anger vilken typ av varning som utfärdas av Aspose.Words när dokumentet laddas eller sparas.

```csharp
[Flags]
public enum WarningType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| DataLossCategory | `FF` | Viss text/tecken/bild eller annan data kommer att saknas antingen i dokumentträdet efter inläsning, eller i det skapade dokumentet efter att det har sparats. |
| DataLoss | `1` | Generisk dataförlust, ingen specifik kod. |
| MajorFormattingLossCategory | `FF00` | Det resulterande dokumentet eller en viss plats i det kan se väsentligt annorlunda ut jämfört med originaldokumentet. |
| MajorFormattingLoss | `100` | Generisk större formateringsförlust, ingen specifik kod. |
| MinorFormattingLossCategory | `FF0000` | Det resulterande dokumentet eller en viss plats i det kan se något annorlunda ut jämfört med originaldokumentet. |
| MinorFormattingLoss | `10000` | Generisk mindre formateringsförlust, ingen specifik kod. |
| FontSubstitution | `20000` | Typsnittet har ersatts. |
| FontEmbedding | `40000` | Förlust av inbäddad teckensnittsinformation när dokumentet sparas. |
| UnexpectedContentCategory | `F000000` | En del innehåll i källdokumentet kunde inte kännas igen (dvs. stöds inte), detta kan orsaka problem eller resultera i data-/formateringsförlust. |
| UnexpectedContent | `1000000` | Generiskt oväntat innehåll, ingen specifik kod. |
| Hint | `10000000` | Informerar om ett potentiellt problem eller föreslår en förbättring. |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
