---
title: Class WarningInfoCollection
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.WarningInfoCollection klass. Representerar en maskinskriven samling avWarningInfo objekt.
type: docs
weight: 6330
url: /sv/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Representerar en maskinskriven samling av[`WarningInfo`](../warninginfo/) objekt.

```csharp
public class WarningInfoCollection : IEnumerable<WarningInfo>, IWarningCallback
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [WarningInfoCollection](warninginfocollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words/warninginfocollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Hämtar ett objekt vid angivet index. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Tar bort alla element från samlingen. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(WarningInfo) | Implementerar[`IWarningCallback`](../iwarningcallback/) gränssnitt. Lägger till en varning för den här samlingen. |

### Anmärkningar

Du kan använda detta samlingsobjekt som den enklaste formen av[`IWarningCallback`](../iwarningcallback/)implementering för att samla in alla varningar som Aspose.Words genererar under en laddnings- eller sparoperation. Skapa en instans av den här klassen och tilldela den till[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) eller[`WarningCallback`](../documentbase/warningcallback/) fast egendom.

### Exempel

Visar hur du ställer in egenskapen för att hitta den närmaste matchningen för ett saknat teckensnitt från tillgängliga teckensnittskällor.

```csharp
[Test]
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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


