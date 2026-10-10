---
title: "Aspose::Words::Fonts::FontFallbackSettings::Load 方法"
linktitle: "加载"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontFallbackSettings::Load 方法。从 XML 流加载回退设置（C++）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fonts/fontfallbacksettings/load/
---
## FontFallbackSettings::Load(const System::SharedPtr\<System::IO::Stream\>\&) method


从 XML 流加载回退设置。

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::SharedPtr<System::IO::Stream> &stream)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 流 | const System::SharedPtr\<System::IO::Stream\>\& | 输入流。 |

## 示例



展示如何从流加载和保存字体回退设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 加载定义一组字体回退设置的 XML 文档。
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font fallback rules.xml", System::IO::FileMode::Open);
    auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
    fontSettings->get_FallbackSettings()->Load(fontFallbackStream);

    doc->set_FontSettings(fontSettings);
}

doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// 使用流将文档当前的字体回退设置保存为 XML 文档。
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FallbackSettings.xml", System::IO::FileMode::Create);
    doc->get_FontSettings()->get_FallbackSettings()->Save(fontFallbackStream);
}
```

## 另见

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Load(const System::String\&) method


从 XML 文件加载字体回退设置。

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::String &fileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 输入文件名。 |

## 示例



展示如何在本地文件系统中加载和保存字体回退设置到/从 XML 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 加载定义一组字体回退设置的 XML 文档。
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_FallbackSettings()->Load(get_MyDir() + u"Font fallback rules.xml");

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// 将文档当前的字体回退设置保存为 XML 文档。
doc->get_FontSettings()->get_FallbackSettings()->Save(get_ArtifactsDir() + u"FallbackSettings.xml");
```

## 另见

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Load(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Load(std::basic_istream<CharType, Traits> &stream)
```

## 另见

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
