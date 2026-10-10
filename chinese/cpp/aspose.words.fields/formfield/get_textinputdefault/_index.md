---
title: "Aspose::Words::Fields::FormField::get_TextInputDefault 方法"
linktitle: "get_TextInputDefault"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FormField::get_TextInputDefault 方法。获取或设置 C++ 中文本表单字段的默认字符串或计算表达式。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


获取或设置文本表单字段的默认字符串或计算表达式。

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
```

## 备注


此属性的含义取决于 [TextInputType](../get_textinputtype/) 属性的值。

当 [TextInputType](../get_textinputtype/) 为 [Regular](../../textformfieldtype/) 或 [Number](../../textformfieldtype/) 时，此字符串指定文本表单字段的默认字符串。当表单字段为空时，此字符串是 Microsoft Word 在文档中显示的内容。

当 [TextInputType](../get_textinputtype/) 为 [Calculated](../../textformfieldtype/) 时，此字符串保存要计算的表达式。该表达式必须符合 Microsoft Word 公式字段的要求。使用此属性设置新表达式时，Aspose.Words 会自动计算公式结果并将其插入表单字段。

Microsoft Word 允许的字符串最长为 255 个字符。
## 另见

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
