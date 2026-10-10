---
title: "Aspose::Words::Fields::FieldAutoNumOut 类"
linktitle: "FieldAutoNumOut"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldAutoNumOut 类。实现 AUTONUMOUT 字段。了解更多，请访问 C++ 文档文章。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.fields/fieldautonumout/
---
## FieldAutoNumOut class


实现 AUTONUMOUT 字段。欲了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldAutoNumOut : public Aspose::Words::Fields::Field
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



展示如何使用 AUTONUMOUT 字段对段落进行编号。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// AUTONUMOUT 字段显示一个在每个 AUTONUMOUT 字段处递增的数字。
// 与 AUTONUM 字段不同，AUTONUMOUT 字段使用大纲编号方案，
// 我们可以在 Microsoft Word 中通过 Format -> Bullets & Numbering -> "Outline Numbered" 来定义它。
// 这使我们能够像编号列表一样自动为项目编号。
// LISTNUM 字段是 AUTONUMOUT 字段的更新替代方案。
// 此字段将显示 "1."。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNumOutline, true);
builder->Writeln(u"\tParagraph 1.");

// 此字段将显示 "2."。
builder->InsertField(Aspose::Words::Fields::FieldType::FieldAutoNumOutline, true);
builder->Writeln(u"\tParagraph 2.");

for (auto&& field : System::IterateOver<Aspose::Words::Fields::FieldAutoNumOut>(doc->get_Range()->get_Fields()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
{
    return f->get_Type() == Aspose::Words::Fields::FieldType::FieldAutoNumOutline;
})))->LINQ_ToList()))
{
    ASSERT_EQ(u" AUTONUMOUT ", field->GetFieldCode());
}

doc->Save(get_ArtifactsDir() + u"Field.AUTONUMOUT.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
