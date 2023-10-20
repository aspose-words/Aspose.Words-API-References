---
title: FieldInfo Class
linktitle: FieldInfo
articleTitle: FieldInfo
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldInfo 班级. 实现 INFO 字段 在 C#.
type: docs
weight: 2080
url: /zh/net/aspose.words.fields/fieldinfo/
---
## FieldInfo class

实现 INFO 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldInfo : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldInfo](fieldinfo/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [InfoType](../../aspose.words.fields/fieldinfo/infotype/) { get; set; } | 获取或设置要插入的文档属性的类型。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [NewValue](../../aspose.words.fields/fieldinfo/newvalue/) { get; set; } | 获取或设置更新属性的可选值。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除该字段。返回字段后面的节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果该字段已被更新，则抛出异常。 |

## 评论

插入有关文档属性的信息。

## 例子

展示如何使用 INFO 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 为“Comments”内置属性设置一个值，然后插入一个 INFO 字段以显示该属性的值。
doc.BuiltInDocumentProperties.Comments = "My comment";
FieldInfo field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.Update();

Assert.AreEqual(" INFO  Comments", field.GetFieldCode());
Assert.AreEqual("My comment", field.Result);

builder.Writeln();

// 为字段的 NewValue 属性设置值并更新
// 该字段还将用新值覆盖相应的内置属性。
field = (FieldInfo)builder.InsertField(FieldType.FieldInfo, true);
field.InfoType = "Comments";
field.NewValue = "New comment";
field.Update();

Assert.AreEqual(" INFO  Comments \"New comment\"", field.GetFieldCode());
Assert.AreEqual("New comment", field.Result);
Assert.AreEqual("New comment", doc.BuiltInDocumentProperties.Comments);

doc.Save(ArtifactsDir + "Field.INFO.docx");
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
