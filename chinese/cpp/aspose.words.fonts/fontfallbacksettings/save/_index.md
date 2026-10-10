---
title: "Aspose::Words::Fonts::FontFallbackSettings::Save 方法"
linktitle: "保存"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontFallbackSettings::Save 方法。将当前回退设置保存到 C++ 中的流。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fonts/fontfallbacksettings/save/
---
## FontFallbackSettings::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


将当前回退设置保存到流中。

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | 输出流。 |

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
## FontFallbackSettings::Save(const System::String\&) method


将当前回退设置保存到文件中。

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::String &fileName)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文件名 | const System::String\& | 输出文件名。 |

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
## FontFallbackSettings::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Save(std::basic_ostream<CharType, Traits> &outputStream)
```

## 另见

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
