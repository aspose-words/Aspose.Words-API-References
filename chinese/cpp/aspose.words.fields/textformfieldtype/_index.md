---
title: "Aspose::Words::Fields::TextFormFieldType 枚举"
linktitle: "TextFormFieldType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::TextFormFieldType 枚举。指定 C++ 中文本表单字段的类型。"
type: docs
weight: 134000
url: /zh/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


指定文本表单字段的类型。

```cpp
enum class TextFormFieldType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Regular | 0 | 文本表单字段可以包含任意文本。 |
| 数字 | 1 | 文本表单字段只能包含数字。 |
| 日期 | 2 | 文本表单字段只能包含有效的日期值。 |
| CurrentDate | 3 | 当字段更新时，文本表单字段的值为当前日期。 |
| CurrentTime | 4 | 当字段更新时，文本表单字段的值为当前时间。 |
| Calculated | 5 | 文本表单字段的值是根据在 [TextInputDefault](../formfield/get_textinputdefault/) 属性中指定的表达式计算得出的。 |


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

## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
