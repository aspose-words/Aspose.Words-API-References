---
title: "Aspose::Words::DocumentBuilder::InsertComboBox 方法"
linktitle: "InsertComboBox"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertComboBox 方法。在 C++ 中于当前位置插入一个组合框表单字段。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


在当前位置插入下拉框表单字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 表单字段的名称。可以是空字符串。长度超过 20 个字符的值将被截断。 |
| items | const System::ArrayPtr\<System::String\>\& | ComboBox 的项目。最多 25 项。 |
| selectedIndex | int32_t | ComboBox 中所选项目的索引。 |

### ReturnValue

刚刚插入的表单字段节点。
## 备注


如果为表单字段指定名称，则会自动创建一个同名的书签。

## 示例



展示如何创建表单字段。
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// 表单字段是文档中的对象，用户可以通过提示输入值与之交互。
// 我们可以使用文档生成器创建它们，下面展示两种实现方式。
// 1 -  基本文本输入：
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  带提示文本的下拉框，以及一系列可能的值：
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```


展示如何在文档中插入组合框表单字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个表单，提示用户从菜单中选择一项。
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## 另见

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
