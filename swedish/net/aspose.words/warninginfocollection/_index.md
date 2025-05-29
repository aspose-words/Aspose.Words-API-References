---
title: WarningInfoCollection Class
linktitle: WarningInfoCollection
articleTitle: WarningInfoCollection
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.WarningInfoCollection, en kraftfull klass för att hantera WarningInfo-objekt, förbättra dokumentbehandling och felhantering.
type: docs
weight: 7490
url: /sv/net/aspose.words/warninginfocollection/
---
## WarningInfoCollection class

Representerar en typad samling av[`WarningInfo`](../warninginfo/) objekt.

För att lära dig mer, besök[Programmering med dokument](https://docs.aspose.com/words/net/programming-with-documents/) dokumentationsartikel.

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
| [Item](../../aspose.words/warninginfocollection/item/) { get; } | Hämtar ett objekt vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clear](../../aspose.words/warninginfocollection/clear/)() | Tar bort alla element från samlingen. |
| [GetEnumerator](../../aspose.words/warninginfocollection/getenumerator/)() | Returnerar ett uppräknarobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [Warning](../../aspose.words/warninginfocollection/warning/)(*[WarningInfo](../warninginfo/)*) | Implementerar[`IWarningCallback`](../iwarningcallback/) gränssnitt. Lägger till en varning i den här samlingen. |

## Anmärkningar

Du kan använda detta samlingsobjekt som den enklaste formen av[`IWarningCallback`](../iwarningcallback/) implementation för att samla alla varningar som Aspose.Words genererar under en laddnings- eller sparoperation. Skapa en instans av denna klass och tilldela den till[`WarningCallback`](../../aspose.words.loading/loadoptions/warningcallback/) eller[`WarningCallback`](../documentbase/warningcallback/) egendom.

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

* class [WarningInfo](../warninginfo/)
* interface [IWarningCallback](../iwarningcallback/)
* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
