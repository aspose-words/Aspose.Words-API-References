---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: 用于 .NET 的 Aspose.Words
description: FontSettings DefaultInstance 财产. 静态默认字体设置 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fonts/fontsettings/defaultinstance/
---
## FontSettings.DefaultInstance property

静态默认字体设置。

```csharp
public static FontSettings DefaultInstance { get; }
```

## 评论

文档中默认使用此实例，除非[`FontSettings`](../../../aspose.words/document/fontsettings/)已指定。

## 例子

演示如何配置默认字体设置实例。

```csharp
// 配置默认字体设置实例以使用“Courier New”字体
// 当我们尝试使用未知字体时作为备用替代品。
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// 该文档没有 FontSettings 配置。当我们渲染文档时，
// 默认的 FontSettings 实例将解决缺少的字体。
// Aspose.Words 将使用“Courier New”来渲染使用未知字体的文本。
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

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

### 也可以看看

* class [FontSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
