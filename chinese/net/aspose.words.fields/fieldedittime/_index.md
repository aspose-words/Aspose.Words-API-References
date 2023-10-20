---
title: FieldEditTime Class
linktitle: FieldEditTime
articleTitle: FieldEditTime
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldEditTime 班级. 实现 EDITTIME 字段 在 C#.
type: docs
weight: 1840
url: /zh/net/aspose.words.fields/fieldedittime/
---
## FieldEditTime class

实现 EDITTIME 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldEditTime : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldEditTime](fieldedittime/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
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

检索自文档创建以来的总编辑时间（以分钟为单位）。

## 例子

演示如何使用 EDITTIME 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// EDITTIME 字段将显示（以分钟为单位）
// 在 Microsoft Word 窗口中打开文档所花费的时间。
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("You've been editing this document for ");
FieldEditTime field = (FieldEditTime)builder.InsertField(FieldType.FieldEditTime, true);
builder.Writeln(" minutes.");

// 这个内置文档属性跟踪分钟。 Microsoft Word 使用此属性
// 跟踪文档打开所花费的时间。我们也可以自己编辑。
doc.BuiltInDocumentProperties.TotalEditingTime = 10;
field.Update();

Assert.AreEqual(" EDITTIME ", field.GetFieldCode());
Assert.AreEqual("10", field.Result);

// 该字段不会实时更新，也必须
// 每当我们需要准确的值时，在 Microsoft Word 中手动更新。
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.EDITTIME.docx");
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
