---
title: "Aspose::Words::Fields::FieldFormText class"
linktitle: "FieldFormText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldFormText 类。实现 FORMTEXT 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 48000
url: /zh/cpp/aspose.words.fields/fieldformtext/
---
## FieldFormText class


实现 FORMTEXT 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldFormText : public Aspose::Words::Fields::Field
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何处理 FORMCHECKBOX、FORMDROPDOWN 和 FORMTEXT 字段。
```cpp
// 这些字段是 FormField 的旧版等价物。我们可以读取，但不能使用 Aspose.Words 创建这些字段。
// 在 Microsoft Word 中，我们可以通过开发者选项卡的“旧版工具”菜单插入这些字段。
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

auto fieldFormCheckBox = System::ExplicitCast<Aspose::Words::Fields::FieldFormCheckBox>(doc->get_Range()->get_Fields()->idx_get(1));
ASSERT_EQ(u" FORMCHECKBOX \u0001", fieldFormCheckBox->GetFieldCode());

auto fieldFormDropDown = System::ExplicitCast<Aspose::Words::Fields::FieldFormDropDown>(doc->get_Range()->get_Fields()->idx_get(2));
ASSERT_EQ(u" FORMDROPDOWN \u0001", fieldFormDropDown->GetFieldCode());

auto fieldFormText = System::ExplicitCast<Aspose::Words::Fields::FieldFormText>(doc->get_Range()->get_Fields()->idx_get(0));
ASSERT_EQ(u" FORMTEXT \u0001", fieldFormText->GetFieldCode());
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
