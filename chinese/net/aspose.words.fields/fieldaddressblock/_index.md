---
title: Class FieldAddressBlock
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.FieldAddressBlock 班级. 实现 ADDRESSBLOCK 字段
type: docs
weight: 1380
url: /zh/net/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class

实现 ADDRESSBLOCK 字段。

```csharp
public class FieldAddressBlock : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldAddressBlock](fieldaddressblock/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段end的节点。 |
| [ExcludedCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/excludedcountryorregionname/) { get; set; } | 获取或设置排除的国家/地区名称。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 得到一个[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [FormatAddressOnCountryOrRegion](../../aspose.words.fields/fieldaddressblock/formataddressoncountryorregion/) { get; set; } | 获取或设置是否根据收件人的国家/地区格式化地址 由 POST*CODE (Universal Postal Union 2006) 定义。 |
| [IncludeCountryOrRegionName](../../aspose.words.fields/fieldaddressblock/includecountryorregionname/) { get; set; } | 获取或设置是否包含国家/地区名称。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LanguageId](../../aspose.words.fields/fieldaddressblock/languageid/) { get; set; } | 获取或设置用于格式化地址的语言 ID。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的LCID。 |
| [NameAndAddressFormat](../../aspose.words.fields/fieldaddressblock/nameandaddressformat/) { get; set; } | 获取或设置名称和地址格式。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（或字段结束，如果没有分隔符）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [GetFieldNames](../../aspose.words.fields/fieldaddressblock/getfieldnames/)() | 返回字段使用的邮件合并字段名称的集合。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回 **无效的**. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update/)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

代表一个地址块。一个地址块是指定信息 的文本块，适用于邮寄地址，按照目的地国家/地区要求的顺序。

### 例子

显示如何获取字段使用的邮件合并字段名称。

```csharp
Document doc = new Document(MyDir + "Field sample - ADDRESSBLOCK.docx");

string[] addressFieldsExpect =
{
    "Company", "First Name", "Middle Name", "Last Name", "Suffix", "Address 1", "City", "State",
    "Country or Region", "Postal Code"
};

FieldAddressBlock addressBlockField = (FieldAddressBlock) doc.Range.Fields[0];
string[] addressBlockFieldNames = addressBlockField.GetFieldNames();
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


