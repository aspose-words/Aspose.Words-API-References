---
title: "Aspose::Words::Lists::ListLabel::get_LabelString 方法"
linktitle: "get_LabelString"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListLabel::get_LabelString 方法。获取列表标签的字符串表示（C++）。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.lists/listlabel/get_labelstring/
---
## ListLabel::get_LabelString method


获取列表标签的字符串表示。

```cpp
System::String Aspose::Words::Lists::ListLabel::get_LabelString()
```


## 示例



展示如何提取所有作为列表项的段落的列表标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

// 查找段落是否属于列表。在我们的文档中，列表使用普通的阿拉伯数字，
// 起始于三，结束于六。
for (auto&& paragraph : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"List item paragraph #{0}", paras->IndexOf(paragraph)) << std::endl;

    // 这是我们在将此节点输出为文本格式时得到的文本。
    // 此文本输出将省略列表标签。去除任何段落格式字符。
    System::String paragraphText = paragraph->ToString(Aspose::Words::SaveFormat::Text).Trim();
    std::cout << System::String::Format(u"\tExported Text: {0}", paragraphText) << std::endl;

    System::SharedPtr<Aspose::Words::Lists::ListLabel> label = paragraph->get_ListLabel();

    // 获取段落在列表当前级别中的位置。如果列表有多个级别，
    // 这将告诉我们它在该级别上的位置。
    std::cout << System::String::Format(u"\tNumerical Id: {0}", label->get_LabelValue()) << std::endl;

    // 将它们组合起来，以在输出中包含列表标签和文本。
    std::cout << System::String::Format(u"\tList label combined with text: {0} {1}", label->get_LabelString(), paragraphText) << std::endl;
}
```

## 另见

* Class [ListLabel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
