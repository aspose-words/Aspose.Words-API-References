---
title: "Aspose::Words::Markup::SdtListItem 类"
linktitle: "SdtListItem"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::SdtListItem 类. 此元素指定父 ComboBox 或 DropDownList 结构化文档标签中的单个列表项。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.markup/sdtlistitem/
---
## SdtListItem class


此元素指定父 [ComboBox](../sdttype/) 或 [DropDownList](../sdttype/) 结构化文档标签中的单个列表项。要了解更多信息，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class SdtListItem : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayText](./get_displaytext/)() const | 获取此列表项的 [Value](./get_value/) 属性内容的替代显示文本。 |
| [get_Value](./get_value/)() const | 获取此列表项的值。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SdtListItem](./sdtlistitem/)(const System::String\&, const System::String\&) | 初始化此类的新实例。 |
| [SdtListItem](./sdtlistitem/)(const System::String\&) | 初始化此类的新实例。 |
| static [Type](./type/)() |  |

## 示例



展示如何使用下拉列表结构化文档标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// 下拉列表结构化文档标签是一种允许用户
// 通过左键单击并在 Microsoft Word 中打开表单，从列表中选择一个选项。
// “ListItems” 属性包含所有列表项，每个列表项都是 “SdtListItem”。
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// 再添加 3 个列表项。使用不同于第一个项的构造函数初始化这些项
// 以显示与其值不同的字符串。
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// 下拉列表正在显示第一个项。将不同的列表项分配给 “SelectedValue” 以显示它。
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// 遍历集合并打印每个元素。
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// 移除最后一个列表项。
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// 由于我们的下拉控件默认显示已移除的项，请为其提供一个存在的项以显示。
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// 使用 “Clear” 方法一次性清空整个下拉项集合。
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
