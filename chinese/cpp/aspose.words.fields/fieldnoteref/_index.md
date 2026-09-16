---
title: "Aspose::Words::Fields::FieldNoteRef 类"
linktitle: "FieldNoteRef"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldNoteRef 类。实现 NOTEREF 字段。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 72000
url: /zh/cpp/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class


实现 NOTEREF 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldNoteRef : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | 获取书签的名称。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_InsertHyperlink](./get_inserthyperlink/)() | 获取是否向书签段落插入超链接。 |
| [get_InsertReferenceMark](./get_insertreferencemark/)() | 插入参考标记，其字符格式与脚注引用或尾注引用样式相同。 |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | 获取是否插入书签段落的相对位置。 |
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
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | 设置书签的名称。 |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | 设置是否向书签段落插入超链接。 |
| [set_InsertReferenceMark](./set_insertreferencemark/)(bool) | 插入参考标记，其字符格式与脚注引用或尾注引用样式相同。 |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | 设置是否插入书签段落的相对位置。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |

## 示例



展示如何使用 NOTEREF 字段交叉引用脚注。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"CrossReference: ");

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldNoteRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNoteRef, false));
// <--- 不要更新字段
field->set_BookmarkName(u"CrossRefBookmark");
field->set_InsertHyperlink(true);
field->set_InsertReferenceMark(true);
field->set_InsertRelativePosition(false);
builder->Writeln();

builder->StartBookmark(u"CrossRefBookmark");
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Cross referenced footnote.");
builder->EndBookmark(u"CrossRefBookmark");
builder->Writeln();

doc->UpdateFields();

// 此字段仅在旧版本的 Microsoft Word 中工作。
doc->Save(get_ArtifactsDir() + u"Field.NOTEREF.doc");
```

## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
