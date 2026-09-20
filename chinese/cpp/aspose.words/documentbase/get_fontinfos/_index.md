---
title: "Aspose::Words::DocumentBase::get_FontInfos 方法"
linktitle: "get_FontInfos"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBase::get_FontInfos 方法。提供对 C++ 中此文档使用的字体属性的访问。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


提供对本文件中使用的字体属性的访问。

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## 备注


此字体定义集合直接从文档中加载。[Font](../../font/) 定义在某些文档中可能是可选的、缺失的或不完整的。

不要依赖此集合来确定文档中是否使用了特定字体。您只能使用此集合获取可能在文档中使用的字体信息。

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

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
