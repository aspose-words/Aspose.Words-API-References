---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs 方法"
linktitle: "get_HeadingPairs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs 方法。指定文档标题及其名称（C++）。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_headingpairs/
---
## BuiltInDocumentProperties::get_HeadingPairs method


指定文档标题及其名称。

```cpp
System::ArrayPtr<System::SharedPtr<System::Object>> Aspose::Words::Properties::BuiltInDocumentProperties::get_HeadingPairs()
```

## 备注


每个标题对在此数组中占用两个元素。

该对的第一个元素是 **String**，指定标题名称。第二个元素是 **Int32**，指定此标题在 [TitlesOfParts](../get_titlesofparts/) 属性中的文档部分计数。

此属性中所有标题对的计数总和必须等于 [TitlesOfParts](../get_titlesofparts/) 属性中的元素数量。

Aspose.Words 不会更新此属性。

## 示例



显示 \"HeadingPairs\" 与 \"TitlesOfParts\" 属性之间的关系。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Heading pairs and titles of parts.docx");

// 我们可以通过以下方式找到这些集合的组合值：
// \"文件\" -> \"属性\" -> \"高级属性\" -> \"内容\" 选项卡。
// HeadingPairs 属性是 <string, int> 对的集合，用于
// 确定一个标题跨越多少文档部分。
System::ArrayPtr<System::SharedPtr<System::Object>> headingPairs = doc->get_BuiltInDocumentProperties()->get_HeadingPairs();

// TitlesOfParts 属性包含属于上述标题的部分名称。
System::ArrayPtr<System::String> titlesOfParts = doc->get_BuiltInDocumentProperties()->get_TitlesOfParts();

int32_t headingPairsIndex = 0;
int32_t titlesOfPartsIndex = 0;
while (headingPairsIndex < headingPairs->get_Length())
{
    std::cout << System::String::Format(u"Parts for {0}:", headingPairs[headingPairsIndex++]) << std::endl;
    int32_t partsCount = System::Convert::ToInt32(headingPairs[headingPairsIndex++]);

    for (int32_t i = 0; i < partsCount; i++)
    {
        std::cout << System::String::Format(u"\t\"{0}\"", titlesOfParts[titlesOfPartsIndex++]) << std::endl;
    }
}
```

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
