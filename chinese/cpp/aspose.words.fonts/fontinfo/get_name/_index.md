---
title: "Aspose::Words::Fonts::FontInfo::get_Name method"
linktitle: "get_Name"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontInfo::get_Name 方法。获取 C++ 中字体的名称。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.fonts/fontinfo/get_name/
---
## FontInfo::get_Name method


获取字体的名称。

```cpp
System::String Aspose::Words::Fonts::FontInfo::get_Name() const
```

## 备注


不能为 **null**。可以是空字符串。

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
