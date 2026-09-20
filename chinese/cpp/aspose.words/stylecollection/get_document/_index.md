---
title: "Aspose::Words::StyleCollection::get_Document method"
linktitle: "get_Document"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::StyleCollection::get_Document 方法。获取 C++ 中的所有者文档。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/stylecollection/get_document/
---
## StyleCollection::get_Document method


获取所属文档。

```cpp
System::SharedPtr<Aspose::Words::DocumentBase> Aspose::Words::StyleCollection::get_Document() const
```


## 示例



展示如何访问文档的样式集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_EQ(4, doc->get_Styles()->get_Count());

// 枚举并列出使用 Aspose.Words 创建的文档默认包含的所有样式。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Style>>> stylesEnum = doc->get_Styles()->GetEnumerator();
    while (stylesEnum->MoveNext())
    {
        System::SharedPtr<Aspose::Words::Style> curStyle = stylesEnum->get_Current();
        std::cout << System::String::Format(u"Style name:\t\"{0}\", of type \"{1}\"", curStyle->get_Name(), curStyle->get_Type()) << std::endl;
        std::cout << System::String::Format(u"\tSubsequent style:\t{0}", curStyle->get_NextParagraphStyleName()) << std::endl;
        std::cout << System::String::Format(u"\tIs heading:\t\t\t{0}", curStyle->get_IsHeading()) << std::endl;
        std::cout << System::String::Format(u"\tIs QuickStyle:\t\t{0}", curStyle->get_IsQuickStyle()) << std::endl;

        ASPOSE_ASSERT_EQ(doc, curStyle->get_Document());
    }
}
```

## 另见

* Class [DocumentBase](../../documentbase/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
