---
title: "Aspose::Words::Document::UpdateListLabels 方法"
linktitle: "UpdateListLabels"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::UpdateListLabels 方法。更新 C++ 中文档所有列表项的列表标签。"
type: docs
weight: 97000
url: /zh/cpp/aspose.words/document/updatelistlabels/
---
## Document::UpdateListLabels method


更新文档中所有列表项的列表标签。

```cpp
void Aspose::Words::Document::UpdateListLabels()
```

## 备注


此方法会为文档中的每个 [ListLabel](../../paragraph/get_listlabel/) 对象更新列表标签属性，例如 [LabelValue](../../../aspose.words.lists/listlabel/get_labelvalue/) 和 [LabelString](../../../aspose.words.lists/listlabel/get_labelstring/)。

此外，在更新文档字段时，此方法有时会被隐式调用。这是必要的，因为某些可能引用列表编号的字段（如 TOC 或 REF）需要保持最新。

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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
