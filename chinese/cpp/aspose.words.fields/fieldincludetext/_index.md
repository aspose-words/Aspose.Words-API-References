---
title: "Aspose::Words::Fields::FieldIncludeText 类"
linktitle: "FieldIncludeText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldIncludeText 类。实现 INCLUDETEXT 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 58000
url: /zh/cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


实现 INCLUDETEXT 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | 获取要包含的文档中书签的名称。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_Encoding](./get_encoding/)() | 获取对引用文件中数据应用的编码。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_LockFields](./get_lockfields/)() override | 获取是否阻止包含的文档中的字段被更新。 |
| [get_MimeType](./get_mimetype/)() | 获取引用文件的 MIME 类型。 |
| [get_NamespaceMappings](./get_namespacemappings/)() override | 获取 XPath 查询的命名空间映射。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_SourceFullName](./get_sourcefullname/)() override | 获取使用 IRI 的文档位置。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| [get_TextConverter](./get_textconverter/)() override | 获取包含文件格式的文本转换器名称。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [get_XPath](./get_xpath/)() override | 获取 XML 文件所需部分的 XPath。 |
| [get_XslTransformation](./get_xsltransformation/)() override | 获取用于格式化 XML 数据的 XSL 转换位置。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | 设置要包含的文档中书签的名称。 |
| [set_Encoding](./set_encoding/)(const System::String\&) | 设置应用于引用文件中数据的编码。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_LockFields](./set_lockfields/)(bool) | 设置是否阻止包含的文档中的字段被更新。 |
| [set_MimeType](./set_mimetype/)(const System::String\&) | 设置引用文件的 MIME 类型。 |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | 设置 XPath 查询的命名空间映射。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | 设置使用 IRI 的文档位置。 |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | 设置包含文件格式的文本转换器名称。 |
| [set_XPath](./set_xpath/)(const System::String\&) | 设置 XML 文件所需部分的 XPath。 |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | 设置用于格式化 XML 数据的 XSL 转换位置。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
