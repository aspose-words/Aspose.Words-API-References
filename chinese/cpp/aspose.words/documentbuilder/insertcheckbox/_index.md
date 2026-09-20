---
title: "Aspose::Words::DocumentBuilder::InsertCheckBox 方法"
linktitle: "InsertCheckBox"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertCheckBox 方法。 在 C++ 中于当前位置插入复选框表单字段。"
type: docs
weight: 31000
url: /zh/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


在当前位置插入复选框表单字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 表单字段的名称。可以是空字符串。长度超过 20 个字符的值将被截断。 |
| checkedValue | bool | 复选框表单字段的选中状态。 |
| size | int32_t | 指定复选框的大小（单位为点）。将其设为 0 可让 MS Word 自动计算复选框的大小。 |

### ReturnValue

刚刚插入的表单字段节点。
## 备注


如果为表单字段指定名称，则会自动创建一个同名的书签。

## 示例



展示如何向文档中插入复选框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入不同大小和默认选中状态的复选框。
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// 表单字段的名称长度限制为 20 个字符。
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// 我们可以在 Microsoft Word 中通过双击这些复选框进行交互。
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## 另见

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


在当前位置插入复选框表单字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| name | const System::String\& | 表单字段的名称。可以是空字符串。长度超过 20 个字符的值将被截断。 |
| defaultValue | bool | 复选框表单字段的默认值。 |
| checkedValue | bool | 复选框表单字段当前的选中状态。 |
| size | int32_t | 指定复选框的大小（单位为点）。将其设为 0 可让 MS Word 自动计算复选框的大小。 |

### ReturnValue

刚刚插入的表单字段节点。
## 备注


如果为表单字段指定名称，则会自动创建一个同名的书签。

## 示例



展示如何向文档中插入复选框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入不同大小和默认选中状态的复选框。
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// 表单字段的名称长度限制为 20 个字符。
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// 我们可以在 Microsoft Word 中通过双击这些复选框进行交互。
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## 另见

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
