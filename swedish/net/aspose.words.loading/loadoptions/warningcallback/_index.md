---
title: LoadOptions.WarningCallback
second_title: Aspose.Words för .NET API Referens
description: LoadOptions fast egendom. Anropas under en laddningsoperation när ett problem upptäcks som kan resultera i förlust av data eller formatering.
type: docs
weight: 170
url: /sv/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Anropas under en laddningsoperation, när ett problem upptäcks som kan resultera i förlust av data eller formatering.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### Exempel

Visar hur man skriver ut och lagrar varningar som uppstår när dokument laddas.

```csharp
public void LoadOptionsWarningCallback()
{
    // Skapa ett nytt LoadOptions-objekt och ställ in dess WarningCallback-attribut
    // som en instans av vår IWarningCallback-implementering.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Vår callback kommer att skriva ut alla varningar som dyker upp under laddningsoperationen.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback som skriver ut varningar och deras detaljer när de uppstår under dokumentladdning.
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
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)


