---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words для .NET
description: LoadOptions WarningCallback свойство. Вызывается во время операции загрузки когда обнаруживается проблема которая может привести к потере точности данных или форматирования на С#.
type: docs
weight: 170
url: /ru/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Вызывается во время операции загрузки, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Примеры

Показывает, как печатать и сохранять предупреждения, возникающие во время загрузки документа.

```csharp
public void LoadOptionsWarningCallback()
{
    // Создаем новый объект LoadOptions и устанавливаем его атрибут WarningCallback
    // как экземпляр нашей реализации IWarningCallback.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Наш обратный вызов будет печатать все предупреждения, возникающие во время операции загрузки.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback, который печатает предупреждения и их подробную информацию по мере их возникновения во время загрузки документа.
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

### Смотрите также

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
