---
title: "Aspose::Words::Fields::FieldLink 类"
linktitle: "FieldLink"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldLink 类。实现 LINK 字段。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 63000
url: /zh/cpp/aspose.words.fields/fieldlink/
---
## FieldLink class


实现 LINK 字段。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldLink : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | 获取是否自动更新此字段。 |
| [get_DisplayResult](../field/get_displayresult/)() | 获取表示显示字段结果的文本。 |
| [get_End](../field/get_end/)() const | 获取表示字段结束的节点。 |
| [get_FieldEnd](../field/get_fieldend/)() const | 获取表示字段结束的节点。 |
| [get_FieldStart](../field/get_fieldstart/)() const | 获取表示字段起始的节点。 |
| [get_Format](../field/get_format/)() | 获取一个 [FieldFormat](../fieldformat/) 对象，提供对字段格式的类型化访问。 |
| [get_FormatUpdateType](./get_formatupdatetype/)() | 获取链接对象更新其格式的方式。 |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | 获取是否将链接对象插入为位图。 |
| [get_InsertAsHtml](./get_insertashtml/)() | 获取是否将链接对象插入为 HTML 格式文本。 |
| [get_InsertAsPicture](./get_insertaspicture/)() | 获取是否将链接对象插入为图片。 |
| [get_InsertAsRtf](./get_insertasrtf/)() | 获取是否将链接对象以富文本格式 (RTF) 插入。 |
| [get_InsertAsText](./get_insertastext/)() | 获取是否将链接对象以纯文本格式插入。 |
| [get_InsertAsUnicode](./get_insertasunicode/)() | 获取是否将链接对象插入为 Unicode 文本。 |
| [get_IsDirty](../field/get_isdirty/)() | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsLinked](./get_islinked/)() | 获取是否通过不在文档中存储图形数据来减小文件大小。 |
| [get_IsLocked](../field/get_islocked/)() | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [get_LocaleId](../field/get_localeid/)() | 获取或设置字段的 LCID。 |
| [get_ProgId](./get_progid/)() | 获取链接信息的应用程序类型。 |
| [get_Result](../field/get_result/)() | 获取或设置位于字段分隔符和字段结束之间的文本。 |
| [get_Separator](../field/get_separator/)() | 获取表示字段分隔符的节点。可以是 **null**。 |
| [get_SourceFullName](./get_sourcefullname/)() | 获取源文件的名称和位置。 |
| [get_SourceItem](./get_sourceitem/)() | 获取正在链接的源文件的部分。 |
| [get_Start](../field/get_start/)() const | 获取表示字段起始的节点。 |
| virtual [get_Type](../field/get_type/)() const | 获取 Microsoft Word 字段类型。 |
| [GetFieldCode](../field/getfieldcode/)() | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../field/getfieldcode/)(bool) | 返回字段起始和字段分隔符之间的文本（如果没有分隔符，则为字段结束之间的文本）。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | 从文档中移除字段。返回字段之后的节点。如果字段的结束是其父节点的最后一个子节点，则返回其父段落。如果字段已经被移除，返回 **null**。 |
| [set_AutoUpdate](./set_autoupdate/)(bool) | 设置是否自动更新此字段。 |
| [set_FormatUpdateType](./set_formatupdatetype/)(const System::String\&) | 设置链接对象更新其格式的方式。 |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | 设置是否将链接对象插入为位图。 |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | 设置是否将链接对象插入为 HTML 格式文本。 |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | 设置是否将链接对象插入为图片。 |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | 设置是否将链接对象以富文本格式 (RTF) 插入。 |
| [set_InsertAsText](./set_insertastext/)(bool) | 设置是否将链接对象以纯文本格式插入。 |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | 设置是否将链接对象插入为 Unicode 文本。 |
| [set_IsDirty](../field/set_isdirty/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/) 的 setter。 |
| [set_IsLinked](./set_islinked/)(bool) | 设置是否通过不在文档中存储图形数据来减小文件大小。 |
| [set_IsLocked](../field/set_islocked/)(bool) | 用于设置 [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/) 的 setter。 |
| [set_LocaleId](../field/set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/) 的 setter。 |
| [set_ProgId](./set_progid/)(const System::String\&) | 设置链接信息的应用程序类型。 |
| [set_Result](../field/set_result/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::Field::get_Result](../field/get_result/) 的 setter。 |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | 设置源文件的名称和位置。 |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | 设置正在链接的源文件的部分。 |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | 执行字段的取消链接。 |
| [Update](../field/update/)() | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
| [Update](../field/update/)(bool) | 执行字段更新。如果字段已经在更新中，则抛出异常。 |
## 另见

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
