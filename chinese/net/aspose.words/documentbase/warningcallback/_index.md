---
title: DocumentBase.WarningCallback
second_title: Aspose.Words for .NET API 参考
description: DocumentBase 财产. 在检测到可能导致 数据或格式保真度损失的问题时在各种文档处理过程中调用
type: docs
weight: 90
url: /zh/net/aspose.words/documentbase/warningcallback/
---
## DocumentBase.WarningCallback property

在检测到可能导致 数据或格式保真度损失的问题时在各种文档处理过程中调用。

```csharp
public IWarningCallback WarningCallback { get; set; }
```

### 评论

文档可能在其存在的任何阶段生成警告，因此尽早设置警告回调 as 以避免警告丢失非常重要。例如这样的属性[`PageCount`](../../document/pagecount/) 实际上构建了稍后用于渲染的文档布局，如果 仅为稍后的渲染调用指定了警告回调，则布局警告可能会丢失。

### 例子

演示如何使用 IWarningCallback 接口来监视字体替换警告。

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // 存储当前字体源集合，这将是每个文档的默认字体源
    // 我们没有为其指定不同的字体源。
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // 出于测试目的，我们将设置 Aspose.Words 仅在不存在的文件夹中查找字体。
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // 渲染文档时，会找不到“Times New Roman”字体的地方。
    // 这将导致字体替换警告，我们的回调将检测到该警告。
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font.", StringComparison.Ordinal));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// 每次加载/保存期间发生警告时调用。
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontSubstitutionWarnings.Warning(info);
    }

    public WarningInfoCollection FontSubstitutionWarnings = new WarningInfoCollection();
}
```

演示如何设置属性以从可用字体源中查找缺失字体的最接近匹配项。

```csharp
public void EnableFontSubstitution()
{
    // 打开一个文档，其中包含使用我们任何字体源中不存在的字体格式化的文本。
    Document doc = new Document(MyDir + "Missing font.docx");

    // 分配一个回调来处理字体替换警告。
    HandleDocumentSubstitutionWarnings substitutionWarningHandler = new HandleDocumentSubstitutionWarnings();
    doc.WarningCallback = substitutionWarningHandler;

    // 设置默认字体名称并启用字体替换。
    FontSettings fontSettings = new FontSettings();
    fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Arial";
    ;
    fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;

    // 字体替换后应使用原始字体规格。
    doc.LayoutOptions.KeepOriginalFontMetrics = true;

    // 如果我们保存缺少字体的文档，我们将收到字体替换警告。
    doc.FontSettings = fontSettings;
    doc.Save(ArtifactsDir + "FontSettings.EnableFontSubstitution.pdf");

    using (IEnumerator<WarningInfo> warnings = substitutionWarningHandler.FontWarnings.GetEnumerator())
        while (warnings.MoveNext())
            Console.WriteLine(warnings.Current.Description);

    // 我们还可以验证集合中的警告并清除它们。
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
    /// 每次加载/保存期间发生警告时调用。
    /// </summary>
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.FontSubstitution)
            FontWarnings.Warning(info);
    }

    public WarningInfoCollection FontWarnings = new WarningInfoCollection();
}
```

### 也可以看看

* interface [IWarningCallback](../../iwarningcallback/)
* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../documentbase/)
* 部件 [Aspose.Words](../../../)


