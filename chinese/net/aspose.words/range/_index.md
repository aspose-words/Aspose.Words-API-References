---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Range 类，轻松管理文档各个部分的关键。通过无缝控制和灵活性增强您的文档处理能力。
type: docs
weight: 5250
url: /zh/net/aspose.words/range/
---
## Range class

代表文档中的连续区域。

要了解更多信息，请访问[使用范围](https://docs.aspose.com/words/net/working-with-ranges/)文档文章。

```csharp
public class Range : IEnumerable<Node>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | 返回[`Bookmarks`](./bookmarks/)代表范围内所有书签的集合。 |
| [Fields](../../aspose.words/range/fields/) { get; } | 返回[`Fields`](./fields/)表示范围内所有字段的集合。 |
| [FormFields](../../aspose.words/range/formfields/) { get; } | 返回[`FormFields`](./formfields/)表示范围内所有表单字段的集合。 |
| [Revisions](../../aspose.words/range/revisions/) { get; } | 获取此范围内存在的修订（跟踪的更改）的集合。 |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | 返回[`StructuredDocumentTags`](./structureddocumenttags/)表示范围内所有结构化文档标签的集合。 |
| [Text](../../aspose.words/range/text/) { get; } | 获取范围的文本。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | 删除范围内的所有字符。 |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | 更改字段类型值[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/)的[`FieldStart`](../../aspose.words.fields/fieldstart/)，[`FieldSeparator`](../../aspose.words.fields/fieldseparator/)，[`FieldEnd`](../../aspose.words.fields/fieldend/) 以便它们与字段代码中包含的字段类型相对应。 |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | 用另一个字符串替换正则表达式指定的字符模式的所有出现。 |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | 用替换字符串替换所有出现的指定字符串模式。 |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 用另一个字符串替换正则表达式指定的字符模式的所有出现。 |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | 用替换字符串替换所有出现的指定字符串模式。 |
| [ToDocument](../../aspose.words/range/todocument/)() | 构造一个包含范围的新的完整文档。 |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | 取消此范围内的字段链接。 |
| [UpdateFields](../../aspose.words/range/updatefields/)() | 更新此范围内的文档字段的值。 |

## 评论

文档由节点树表示，并且节点提供 operations 来与树一起工作，但如果将 document 视为连续的文本序列，则某些操作更容易执行。

`Range`是一个“外观”接口，它提供将 document 或文档的各部分视为“平面”文本的方法，而不管 document 节点是否存储在树状对象模型中。

`Range`不包含任何文本或节点，它仅仅是文档片段上的视图或“窗口” 。

## 例子

展示如何获取某个范围覆盖的所有节点的文本内容。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### 也可以看看

* class [Node](../node/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
