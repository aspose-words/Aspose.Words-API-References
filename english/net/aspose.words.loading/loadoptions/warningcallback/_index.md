---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words for .NET
description: Discover the LoadOptions WarningCallback property, which alerts you during load operations to prevent data loss and ensure formatting integrity.
type: docs
weight: 180
url: /net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Examples

Shows how to print and store warnings that occur during document loading.

```csharp
public void LoadOptionsWarningCallback()
{
    // Create a new LoadOptions object and set its WarningCallback attribute
    // as an instance of our IWarningCallback implementation.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Our callback will print all warnings that come up during the load operation.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.That(warnings.Count, Is.EqualTo(3));
}

/// <summary>
/// IWarningCallback that prints warnings and their details as they arise during document loading.
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

### See Also

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
