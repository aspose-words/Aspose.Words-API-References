---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LoadOptions WarningCallback, которое предупреждает вас во время операций загрузки, чтобы предотвратить потерю данных и обеспечить целостность форматирования.
type: docs
weight: 180
url: /ru/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Примеры

Показывает, как распечатать и сохранить предупреждения, возникающие во время загрузки документа.

```csharp
public void LoadOptionsWarningCallback()
{
    // Создайте новый объект LoadOptions и установите его атрибут WarningCallback
    // как экземпляр нашей реализации IWarningCallback.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Наш обратный вызов выведет все предупреждения, которые возникнут во время операции загрузки.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback, который выводит предупреждения и их подробности по мере их возникновения во время загрузки документа.
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
