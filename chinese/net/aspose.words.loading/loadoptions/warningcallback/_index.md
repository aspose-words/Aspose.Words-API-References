---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words for .NET
description: 发现 LoadOptions WarningCallback 属性，该属性会在加载操作期间提醒您，以防止数据丢失并确保格式完整性。
type: docs
weight: 180
url: /zh/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

在加载操作期间调用，当检测到可能导致数据或格式保真度损失的问题时。

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## 例子

显示如何打印和存储文档加载期间出现的警告。

```csharp
public void LoadOptionsWarningCallback()
{
    // 创建一个新的 LoadOptions 对象并设置其 WarningCallback 属性
    // 作为我们的 IWarningCallback 实现的一个实例。
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // 我们的回调将打印加载操作期间出现的所有警告。
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback 在文档加载过程中打印警告及其详细信息。
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

### 也可以看看

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
