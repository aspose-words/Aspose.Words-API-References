---
title: "Aspose::Words::Style::get_Name 方法"
linktitle: "get_Name"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Style::get_Name 方法。获取或设置 C++ 中样式的名称。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words/style/get_name/
---
## Style::get_Name method


获取或设置样式的名称。

```cpp
System::String Aspose::Words::Style::get_Name() const
```

## 备注


不能为空字符串。

如果集合中已经存在同名样式，则此样式将覆盖它。所有受影响的节点将引用新样式。

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


展示如何克隆文档的样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// AddCopy 方法创建指定样式的副本，并
// 自动为该样式生成新名称，例如 "Heading 1_0"。
System::SharedPtr<Aspose::Words::Style> newStyle = doc->get_Styles()->AddCopy(doc->get_Styles()->idx_get(u"Heading 1"));

// 使用样式的 "Name" 属性更改样式的标识名称。
newStyle->set_Name(u"My Heading 1");

// 我们的文档现在有两个外观相同但名称不同的样式。
// 更改其中一个样式的设置不会影响另一个。
newStyle->get_Font()->set_Color(System::Drawing::Color::get_Red());

ASSERT_EQ(u"My Heading 1", newStyle->get_Name());
ASSERT_EQ(u"Heading 1", doc->get_Styles()->idx_get(u"Heading 1")->get_Name());

ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Type(), newStyle->get_Type());
ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Name(), newStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Size(), newStyle->get_Font()->get_Size());
ASPOSE_ASSERT_NE(doc->get_Styles()->idx_get(u"Heading 1")->get_Font()->get_Color(), newStyle->get_Font()->get_Color());
```

## 另见

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
