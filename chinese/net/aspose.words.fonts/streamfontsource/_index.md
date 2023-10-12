---
title: Class StreamFontSource
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fonts.StreamFontSource 班级. 用户定义流字体源的基类
type: docs
weight: 3040
url: /zh/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

用户定义流字体源的基类。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public abstract class StreamFontSource : FontSourceBase
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | 缓存中此源的键。 |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | 返回字体源优先级。 |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | 返回字体源的类型。 |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | 在处理字体源期间检测到可能导致格式保真度损失的问题时调用。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | 此方法应根据需要打开包含字体数据的流。 |

### 评论

为了使用流字体源，您应该从`StreamFontSource` 并提供实施[`OpenFontDataStream`](./openfontdatastream/)方法。

[`OpenFontDataStream`](./openfontdatastream/)方法可以被调用多次。当 Aspose.Words 扫描提供的字体源以获取可用字体列表时，它将第一次被称为 。稍后，如果文档中使用了 字体，则可能会调用它来解析字体数据并将字体数据嵌入到某些输出格式中。

`StreamFontSource`可能很有用，因为它允许仅在需要时加载字体数据 ，而不是将其存储在内存中[`FontSettings`](../fontsettings/)寿命。

### 例子

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

* class [FontSourceBase](../fontsourcebase/)
* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)


