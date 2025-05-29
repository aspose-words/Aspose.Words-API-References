---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words für .NET
description: Entdecken Sie die LoadOptions WarningCallback-Eigenschaft, die Sie während Ladevorgängen warnt, um Datenverlust zu verhindern und die Formatierungsintegrität sicherzustellen.
type: docs
weight: 180
url: /de/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Wird während eines Ladevorgangs aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Daten- oder Formatierungsgenauigkeit führen kann.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Beispiele

Zeigt, wie Warnungen, die beim Laden von Dokumenten auftreten, gedruckt und gespeichert werden.

```csharp
public void LoadOptionsWarningCallback()
{
    // Erstellen Sie ein neues LoadOptions-Objekt und legen Sie sein WarningCallback-Attribut fest
    // als Instanz unserer IWarningCallback-Implementierung.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Unser Rückruf druckt alle Warnungen aus, die während des Ladevorgangs auftreten.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback, das Warnungen und ihre Details druckt, wenn sie beim Laden des Dokuments auftreten.
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

### Siehe auch

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
