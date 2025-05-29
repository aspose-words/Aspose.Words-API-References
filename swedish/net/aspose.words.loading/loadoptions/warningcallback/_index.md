---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LoadOptions WarningCallback, som varnar dig under inläsningsåtgärder för att förhindra dataförlust och säkerställa formateringens integritet.
type: docs
weight: 180
url: /sv/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Anropas under en inläsningsoperation, när ett problem upptäcks som kan leda till förlust av data- eller formateringsåtergivning.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Exempel

Visar hur man skriver ut och lagrar varningar som uppstår vid dokumentinläsning.

```csharp
public void LoadOptionsWarningCallback()
{
    // Skapa ett nytt LoadOptions-objekt och ange dess WarningCallback-attribut
    // som en instans av vår IWarningCallback-implementering.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Vår återanropsfunktion skriver ut alla varningar som uppstår under laddningsoperationen.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback som skriver ut varningar och deras detaljer allt eftersom de uppstår under dokumentinläsning.
/// </summary>
private class DocumentLoadingWarningCallback : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        Console.WriteLine($"Warning: {info.WarningType}");
        Console.WriteLine($"\tSource: {info.Source}");
        Console.WriteLine($"\tDescription: {info.Description}");
        mWarnings.Add(info);
    }

    public List<WarningInfo> GetWarnings()
    {
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Se även

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
