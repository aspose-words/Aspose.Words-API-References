---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words per .NET
description: Scopri la proprietà LoadOptions WarningCallback, che ti avvisa durante le operazioni di caricamento per evitare la perdita di dati e garantire l'integrità della formattazione.
type: docs
weight: 180
url: /it/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Chiamato durante un'operazione di caricamento, quando viene rilevato un problema che potrebbe causare la perdita di fedeltà dei dati o della formattazione.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Esempi

Mostra come stampare e memorizzare gli avvisi che si verificano durante il caricamento dei documenti.

```csharp
public void LoadOptionsWarningCallback()
{
    // Crea un nuovo oggetto LoadOptions e imposta il suo attributo WarningCallback
    // come istanza della nostra implementazione IWarningCallback.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Il nostro callback stamperà tutti gli avvisi che si presentano durante l'operazione di caricamento.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback che stampa gli avvisi e i relativi dettagli non appena si presentano durante il caricamento del documento.
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

### Guarda anche

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
