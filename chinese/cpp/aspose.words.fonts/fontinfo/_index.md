---
title: "Aspose::Words::Fonts::FontInfo 类"
linktitle: "FontInfo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfo 类。指定文档中使用的字体信息。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.fonts/fontinfo/
---
## FontInfo class


指定文档中使用的字体信息。要了解更多信息，请访问 [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) 文档文章。

```cpp
class FontInfo : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AltName](./get_altname/)() const | 获取或设置字体的别名。 |
| [get_Charset](./get_charset/)() | 获取或设置字体的字符集。 |
| [get_EmbeddingLicensingRights](./get_embeddinglicensingrights/)() | 获取嵌入字体的许可权利。 |
| [get_Family](./get_family/)() const | 获取或设置此字体所属的字体族。 |
| [get_IsTrueType](./get_istruetype/)() const | 指示此字体是 TrueType 或 OpenType 字体，而非光栅或矢量字体。默认是 **true**。 |
| [get_Name](./get_name/)() const | 获取字体的名称。 |
| [get_Panose](./get_panose/)() const | 获取或设置 PANOSE 字体分类编号。 |
| [get_Pitch](./get_pitch/)() const | 字距指示字体是固定字距、比例间距，还是依赖默认设置。 |
| [GetEmbeddedFont](./getembeddedfont/)(Aspose::Words::Fonts::EmbeddedFontFormat, Aspose::Words::Fonts::EmbeddedFontStyle) | 获取特定的嵌入式字体文件。 |
| [GetEmbeddedFontAsOpenType](./getembeddedfontasopentype/)(Aspose::Words::Fonts::EmbeddedFontStyle) | 获取 OpenType 格式的嵌入式字体文件。 [Fonts](../) 中的嵌入式 OpenType 格式会被转换为 OpenType。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AltName](./set_altname/)(const System::String\&) | 设置器用于 [Aspose::Words::Fonts::FontInfo::get_AltName](./get_altname/)。 |
| [set_Charset](./set_charset/)(int32_t) | 设置器用于 [Aspose::Words::Fonts::FontInfo::get_Charset](./get_charset/)。 |
| [set_Family](./set_family/)(Aspose::Words::Fonts::FontFamily) | 设置器用于 [Aspose::Words::Fonts::FontInfo::get_Family](./get_family/)。 |
| [set_IsTrueType](./set_istruetype/)(bool) | 设置器用于 [Aspose::Words::Fonts::FontInfo::get_IsTrueType](./get_istruetype/)。 |
| [set_Panose](./set_panose/)(const System::ArrayPtr\<uint8_t\>\&) | 设置器用于 [Aspose::Words::Fonts::FontInfo::get_Panose](./get_panose/)。 |
| [set_Pitch](./set_pitch/)(Aspose::Words::Fonts::FontPitch) | 设置器用于 [Aspose::Words::Fonts::FontInfo::get_Pitch](./get_pitch/)。 |
| static [Type](./type/)() |  |
## 备注


您不能直接创建此类的实例。请使用 [FontInfos](../../aspose.words/documentbase/get_fontinfos/) 属性来访问文档中定义的字体集合。

## 示例



展示如何打印文档中存在的字体详细信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// 打印文档中所有已使用和未使用的字体。
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## 另见

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
