---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts 方法"
linktitle: "get_EmbedSystemFonts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts 方法。指定是否将系统字体嵌入文档。此属性的默认值为 false。此选项仅在 C++ 中将 EmbedTrueTypeFonts 选项设置为 true 时有效。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


指定是否将系统字体嵌入文档。此属性的默认值为 **false**。此选项仅在 [EmbedTrueTypeFonts](../get_embedtruetypefonts/) 选项设置为 **true** 时有效。

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## 备注


将此属性设置为 **true** 在用户使用东亚系统且希望创建的文档能够在没有该语言字体的其他系统上阅读时非常有用。例如，使用日语系统的用户可以选择在文档中嵌入字体，从而使该日语文档在所有系统上均可阅读。

此选项仅适用于 DOC、DOCX 和 RTF 格式。

## 示例



展示如何保存带有嵌入 TrueType 字体的文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## 另见

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
