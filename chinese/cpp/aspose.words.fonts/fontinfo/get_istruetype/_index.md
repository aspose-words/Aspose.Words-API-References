---
title: "Aspose::Words::Fonts::FontInfo::get_IsTrueType 方法"
linktitle: "get_IsTrueType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfo::get_IsTrueType 方法。指示此字体是 TrueType 或 OpenType 字体，而不是光栅或矢量字体。默认在 C++ 中为 true。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


指示此字体是 TrueType 或 OpenType 字体，而非光栅或矢量字体。默认是 **true**。

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


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

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
