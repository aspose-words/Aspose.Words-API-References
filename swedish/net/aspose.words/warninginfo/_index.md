---
title: Class WarningInfo
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.WarningInfo klass. Innehåller information om en varning som Aspose.Words utfärdade när dokument laddades eller sparades.
type: docs
weight: 6630
url: /sv/net/aspose.words/warninginfo/
---
## WarningInfo class

Innehåller information om en varning som Aspose.Words utfärdade när dokument laddades eller sparades.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

```csharp
public class WarningInfo
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Description](../../aspose.words/warninginfo/description/) { get; } | Returnerar beskrivningen av varningen. |
| [Source](../../aspose.words/warninginfo/source/) { get; } | Returnerar källan till varningen. |
| [WarningType](../../aspose.words/warninginfo/warningtype/) { get; } | Returnerar typen av varning. |

### Anmärkningar

Du skapar inte instanser av den här klassen. Objekt i denna klass skapas och skickas av Aspose.Words till[`Warning`](../iwarningcallback/warning/) metod.

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


