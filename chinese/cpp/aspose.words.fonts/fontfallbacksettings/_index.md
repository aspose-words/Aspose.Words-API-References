---
title: "Aspose::Words::Fonts::FontFallbackSettings 类"
linktitle: "FontFallbackSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontFallbackSettings 类。指定字体回退机制的设置。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class


指定字体回退机制设置。要了解更多信息，请访问 [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) 文档文章。

```cpp
class FontFallbackSettings : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [BuildAutomatic](./buildautomatic/)() | 自动通过扫描可用字体来构建回退设置。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | 从 XML 文件加载字体回退设置。 |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | 从 XML 流加载回退设置。 |
| [Load](./load/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [LoadMsOfficeFallbackSettings](./loadmsofficefallbacksettings/)() | 加载预定义的回退设置，该设置模拟 Microsoft Word 的回退并使用 Microsoft Office 字体。 |
| [LoadNotoFallbackSettings](./loadnotofallbacksettings/)() | 加载使用 Google Noto 字体的预定义回退设置。 |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | 将当前回退设置保存到流中。 |
| [Save](./save/)(const System::String\&) | 将当前回退设置保存到文件中。 |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

## 示例



展示如何在 Unicode 字符码范围内分配回退字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// 将我们的字体设置配置为仅从 "MyFonts" 文件夹获取字体。
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// 调用 "BuildAutomatic" 方法将生成一个回退方案，
// 尽可能在更多的 Unicode 字符码之间分配可访问的字体。
// 在我们的案例中，它只能访问位于 "MyFonts" 文件夹中的少量字体。
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// 我们也可以从类似的文件加载自定义替代方案。
// 此方案将在 "0000-00ff" Unicode 区块中使用 "AllegroOpen" 字体，在 "0100-024f" 区块中也使用 "AllegroOpen" 字体，
// 并在方案中其他字体未覆盖的所有其他范围使用 "M+ 2m" 字体。
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// 创建文档构建器并将其字体设置为我们任何来源中不存在的字体。
// 我们的字体设置将在使用不可用字体输入字符时调用回退方案。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// 使用构建器打印从 0x0021 到 0x052F 的每个 Unicode 字符，
// 并使用描述性行划分我们在自定义字体回退方案中定义的 Unicode 区块。
for (int32_t i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder->Writeln(u"\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;

        case 0x0100:
            builder->Writeln(u"\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;

        case 0x0250:
            builder->Writeln(u"\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;

    }

    builder->Write(System::String::Format(u"{0}", System::Convert::ToChar(i)));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.pdf");
```

## 另见

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
