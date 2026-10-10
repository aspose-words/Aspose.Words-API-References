---
title: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts 方法"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts 方法。指定在保存文档时是否嵌入 TrueType 字体。此属性在 C++ 中的默认值为 false。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


指定在保存文档时是否嵌入 TrueType 字体。此属性的默认值为 **false**。

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## 备注


嵌入 TrueType 字体可以让其他人在查看文档时使用创建时相同的字体，但可能会显著增加文档大小。

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
