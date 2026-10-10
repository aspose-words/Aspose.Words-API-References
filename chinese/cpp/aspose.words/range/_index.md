---
title: "Aspose::Words::Range 类"
linktitle: "范围"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Range 类。表示文档中的连续区域。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 51000
url: /zh/cpp/aspose.words/range/
---
## Range class


表示文档中的连续区域。要了解更多，请访问 [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/) 文档文章。

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Delete](./delete/)() | 删除范围内的所有字符。 |
| [get_Bookmarks](./get_bookmarks/)() | 返回一个 [Bookmarks](./get_bookmarks/) 集合，表示范围内的所有书签。 |
| [get_Fields](./get_fields/)() | 返回一个 [Fields](./get_fields/) 集合，表示范围内的所有字段。 |
| [get_FormFields](./get_formfields/)() | 返回一个 [FormFields](./get_formfields/) 集合，表示范围内的所有表单字段。 |
| [get_Revisions](./get_revisions/)() | 获取此范围内存在的修订（已跟踪更改）集合。 |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | 返回一个 [StructuredDocumentTags](./get_structureddocumenttags/) 集合，表示范围内的所有结构化文档标签。 |
| [get_Text](./get_text/)() | 获取范围的文本。 |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | 更改此范围内 [FieldStart](../../aspose.words.fields/fieldstart/)、[FieldSeparator](../../aspose.words.fields/fieldseparator/)、[FieldEnd](../../aspose.words.fields/fieldend/) 的字段类型值 [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/)，使其对应于字段代码中包含的字段类型。 |
| [Replace](./replace/)(const System::String\&, const System::String\&) | 将指定字符字符串模式的所有出现替换为替换字符串。 |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 将正则表达式指定的字符模式的所有出现替换为另一个字符串。 |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 将指定字符字符串模式的所有出现替换为替换字符串。 |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 将正则表达式指定的字符模式的所有出现替换为另一个字符串。 |
| [ToDocument](./todocument/)() | 构造一个包含该范围的完整文档。 |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | 解除此范围内字段的链接。 |
| [UpdateFields](./updatefields/)() | 更新此范围内文档字段的值。 |
## 备注


文档由节点树表示，节点提供对树进行操作的功能，但如果将文档视为连续的文本序列，某些操作会更容易执行。

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## 示例



展示如何获取范围覆盖的所有节点的文本内容。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
