---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: 用于 .NET 的 Aspose.Words
description: StreamFontSource OpenFontDataStream 方法. 此方法应根据需要打开包含字体数据的流 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

此方法应根据需要打开包含字体数据的流。

```csharp
public abstract Stream OpenFontDataStream()
```

### 返回值

字体数据流。

## 评论

读取后流将关闭。无需显式关闭它。

## 例子

展示如何从流加载字体。

```csharp
public void StreamFontSourceFileRendering()
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// 仅在需要时加载字体数据而不是将其存储在内存中
/// 在“FontSettings”对象的整个生命周期内。
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### 也可以看看

* class [StreamFontSource](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
