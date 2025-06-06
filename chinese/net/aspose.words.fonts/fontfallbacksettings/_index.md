---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fonts.FontFallbackSettings 以获得可自定义的字体后备选项，确保无缝文档渲染和增强文本显示。
type: docs
weight: 3330
url: /zh/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

指定字体回退机制设置。

要了解更多信息，请访问[使用字体](https://docs.aspose.com/words/net/working-with-fonts/)文档文章。

```csharp
public class FontFallbackSettings
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | 通过扫描可用字体自动构建后备设置。 |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | 从 XML 流加载后备设置。 |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | 从 XML 文件加载字体后备设置。 |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | 加载预定义的后备设置，模仿 Microsoft Word 后备并使用 Microsoft Office 字体。 |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | 加载使用 Google Noto 字体的预定义后备设置。 |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | 将当前后备设置保存到流。 |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | 将当前后备设置保存到文件。 |

## 评论

默认情况下，后备设置是使用预定义设置初始化的，模仿 Microsoft Word 后备。

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

* 命名空间 [Aspose.Words.Fonts](../../aspose.words.fonts/)
* 部件 [Aspose.Words](../../)
