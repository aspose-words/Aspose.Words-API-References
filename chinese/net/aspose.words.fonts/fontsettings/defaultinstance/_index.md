---
title: FontSettings.DefaultInstance
linktitle: DefaultInstance
articleTitle: DefaultInstance
second_title: Aspose.Words for .NET
description: 探索 FontSettings DefaultInstance 属性，简化静态字体管理。使用可自定义的默认设置优化您的设计！
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

默认情况下，此实例在文档中被使用，除非[`FontSettings`](../../../aspose.words/document/fontsettings/)已指定。

## 例子

展示如何配置默认字体设置实例。

```csharp
// 配置默认字体设置实例以使用“Courier New”字体
// 当我们尝试使用未知字体时作为备用替代品。
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.Enabled);

Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Non-existent font";
builder.Write("Hello world!");

// 此文档没有 FontSettings 配置。当我们渲染文档时，
// 默认的 FontSettings 实例将解决丢失的字体。
// Aspose.Words 将使用“Courier New”来呈现使用未知字体的文本。
Assert.Null(doc.FontSettings);

doc.Save(ArtifactsDir + "FontSettings.DefaultFontInstance.pdf");
```

展示如何使用 IWarningCallback 接口监视字体替换警告。

```csharp
public void SubstitutionWarning()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Font.Name = "Times New Roman";
    builder.Writeln("Hello world!");

    FontSubstitutionWarningCollector callback = new FontSubstitutionWarningCollector();
    doc.WarningCallback = callback;

    // 存储当前的字体源集合，这将是每个文档的默认字体源
    // 我们没有指定不同的字体源。
    FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

    // 为了测试目的，我们将设置 Aspose.Words 仅在不存在的文件夹中查找字体。
    FontSettings.DefaultInstance.SetFontsFolder(string.Empty, false);

    // 在渲染文档时，将没有地方找到“Times New Roman”字体。
    // 这将导致字体替换警告，我们的回调将会检测到。
    doc.Save(ArtifactsDir + "FontSettings.SubstitutionWarning.pdf");

    FontSettings.DefaultInstance.SetFontsSources(originalFontSources);

    Assert.True(callback.FontSubstitutionWarnings[0].WarningType == WarningType.FontSubstitution);
    Assert.True(callback.FontSubstitutionWarnings[0].Description
        .Equals(
            "Font 'Times New Roman' has not been found. Using 'Fanwood' font instead. Reason: first available font."));
}

private class FontSubstitutionWarningCollector : IWarningCallback
{
    /// <summary>
    /// 每次加载/保存期间出现警告时调用。
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
