---
title: "Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts 方法"
linktitle: "get_SaveSubsetFonts"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts 方法。指定是否将嵌入的 TrueType 字体的子集随文档一起保存。此属性的默认值为 false。此选项仅在 C++ 中将 EmbedTrueTypeFonts 属性设置为 true 时有效。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


指定是否将嵌入的 TrueType 字体的子集随文档一起保存。此属性的默认值为 **false**。此选项仅在 [EmbedTrueTypeFonts](../get_embedtruetypefonts/) 属性设置为 **true** 时有效。

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


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
