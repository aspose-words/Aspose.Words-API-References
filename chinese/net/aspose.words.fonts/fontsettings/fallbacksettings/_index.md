---
title: FontSettings.FallbackSettings
linktitle: FallbackSettings
articleTitle: FallbackSettings
second_title: Aspose.Words for .NET
description: 探索 FontSettings FallbackSettings 属性，优化字体回退机制。无缝文本渲染，提升您的设计体验！
type: docs
weight: 30
url: /zh/net/aspose.words.fonts/fontsettings/fallbacksettings/
---
## FontSettings.FallbackSettings property

与字体回退机制相关的设置。

```csharp
public FontFallbackSettings FallbackSettings { get; }
```

## 例子

展示如何在 Unicode 字符代码范围内分布后备字体。

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// 配置我们的字体设置以仅从“MyFonts”文件夹中获取字体。
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// 调用“BuildAutomatic”方法将生成一个后备方案，
// 将可访问的字体分布在尽可能多的 Unicode 字符代码中。
// 在我们的例子中，它只能访问“MyFonts”文件夹中的少数字体。
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// 我们还可以从这样的文件中加载自定义替换方案。
// 此方案将“AllegroOpen”字体应用于“0000-00ff”Unicode 块，将“AllegroOpen”字体应用于“0100-024f”，
// 以及方案中其他字体未涵盖的所有其他范围内的“M+ 2m”字体。
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// 创建一个文档构建器并将其字体设置为我们任何源中都不存在的字体。
// 我们的字体设置将为使用不可用字体输入的字符调用后备方案。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// 使用构建器打印从 0x0021 到 0x052F 的每个 Unicode 字符，
// 使用描述性线条划分我们在自定义字体后备方案中定义的 Unicode 块。
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### 也可以看看

* class [FontFallbackSettings](../../fontfallbacksettings/)
* class [FontSettings](../)
* 命名空间 [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../../)
