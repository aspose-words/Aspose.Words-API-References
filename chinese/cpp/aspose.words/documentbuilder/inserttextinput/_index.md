---
title: "Aspose::Words::DocumentBuilder::InsertTextInput method"
linktitle: "InsertTextInput"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertTextInput 方法。 在 C++ 中于当前位置插入文本表单字段。"
type: docs
weight: 49000
url: /zh/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


在当前位置插入文本表单字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 表单字段的名称。 可以是空字符串。 |
| 类型 | Aspose::Words::Fields::TextFormFieldType | 指定文本表单字段的类型。 |
| 格式 | const System::String\& | 用于格式化表单字段值的格式字符串。 |
| fieldValue | const System::String\& | 将在字段中显示的文本。 |
| maxLength | int32_t | 用户在表单字段中可以输入的最大长度。 设置为零表示无限长度。 |

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


展示如何在文档中插入文本输入表单字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入一个提示用户输入文本的表单。
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


展示如何插入文本输入表单字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// 插入一个文本输入字段，允许用户点击并输入文本。
// 分配一些占位文本，用户可以覆盖并传递
// 将最大文本长度设为 0，以对表单字段内容不设限制。
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// 表单字段将以 \"input\" HTML 标签的形式出现，type 为 \"text\"。
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## 另见

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
