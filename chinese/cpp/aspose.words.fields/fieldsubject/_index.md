---
title: "Aspose::Words::Fields::FieldSubject 类"
linktitle: "FieldSubject"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSubject 类。实现 SUBJECT 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 97000
url: /zh/cpp/aspose.words.fields/fieldsubject/
---
## FieldSubject class


实现 SUBJECT 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldSubject : public Aspose::Words::Fields::Field
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
| [get_Text](./get_text/)() | 获取或设置主题的文本。 |
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
| [set_Text](./set_text/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldSubject::get_Text](./get_text/) 的设置器。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何使用 SUBJECT 字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 为文档的 \"Subject\" 内置属性设置值。
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// 创建一个 SUBJECT 字段以显示该内置属性的值。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// 如果我们为 SUBJECT 字段的 Text 属性赋值并更新它，字段将
// 使用其 Text 属性的值覆盖 \"Subject\" 内置属性的当前值，
// 然后显示新值。
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
